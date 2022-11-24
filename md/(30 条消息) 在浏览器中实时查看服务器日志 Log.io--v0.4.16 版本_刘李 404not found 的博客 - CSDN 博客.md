> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [blog.csdn.net](https://blog.csdn.net/qq_39680564/article/details/116453370)

### 文章目录

*   [一、Log.io 介绍](#Logio_1)
*   [二、搭建准备](#_6)
*   [三、安装服务端](#_31)
*   [四、安装客户端](#_73)

一、Log.io 介绍
===========

官网地址：[http://logio.org](http://logio.org/)  
github 地址：[https://github.com/NarrativeScience/log.io](https://github.com/NarrativeScience/log.io)  
![](https://img-blog.csdnimg.cn/20210506160113961.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM5NjgwNTY0,size_16,color_FFFFFF,t_70)  
简单理解为：可以使用浏览器实时查看服务器上的日志，但是看不了历史的日志，类似于`tail -f`命令。

二、搭建准备
======

`Server`服务端：接受客户端发送过来的日志  
`Input`客户端：用于日志采集，将日志信息发送到服务端

<table><thead><tr><th>角色</th><th>IP</th><th>Node 版本</th><th>log.io 版本</th></tr></thead><tbody><tr><td>服务端</td><td>192.168.1.141</td><td>&gt;= 12</td><td>log.io@0.4.16</td></tr><tr><td>客户端</td><td>192.168.1.140</td><td>&gt;= 12</td><td>log.io-file-input@0.4.16</td></tr></tbody></table>

关闭防火墙

```
systemctl stop firewalld.service
```

安装 [node](https://so.csdn.net/so/search?q=node&spm=1001.2101.3001.7020).js

```
curl -fsSL https://rpm.nodesource.com/setup_12.x | bash -
yum install -y nodejs
```

查看

```
[root@localhost ~]# npm -v && node -v
6.14.12
v12.22.1
```

三、安装服务端
=======

```
npm install -g log.io --registry https://registry.npm.taobao.org
```

创建配置文件，新版本`v0.4.16`已经不会自动生成配置文件了

```
mkdir -p ~/.log.io/
vi ~/.log.io/server.json
```

`users`中为登录的用户名和密码

```
{
  "messageServer": {
    "port": 6689,
    "host": "0.0.0.0"
  },
  "httpServer": {
    "port": 6688,
    "host": "0.0.0.0"
  },
  "debug": false,
  "basicAuth": {
    "realm": "abc123xyz",
    "users": {
      "admin": "admin123",
      "user123": "user123"
    }
  }
}
```

启动服务端命令`log.io-server`

```
[root@localhost ~]# log.io-server
TCP message server listening on port 6689
HTTP server listening on port 6688
```

浏览器访问 `http://192.168.1.141:6688`  
![](https://img-blog.csdnimg.cn/2021050615344113.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM5NjgwNTY0,size_16,color_FFFFFF,t_70)

四、安装客户端
=======

```
npm install -g log.io-file-input --registry https://registry.npm.taobao.org
```

创建配置文件

```
mkdir ~/.log.io/inputs/
vi ~/.log.io/inputs/file.json
```

输入路径可以是文件路径、目录路径或 glob。

```
{
  "messageServer": {
    "host": "192.168.1.141",
    "port": 6689
  },
  "inputs": [
    {
      "source": "192.168.1.140",
      "stream": "eureka",
      "config": {
        "path": "/opt/logs/eureka.log"
      }
    },
    {
      "source": "192.168.1.140",
      "stream": "saas-ws",
      "config": {
        "path": "/opt/saas-ws.log"
      }
    },
    {
      "source": "192.168.1.140",
      "stream": "base-ms",
      "config": {
        "path": "/opt/base-ms.log"
      }
    }
  ]
}
```

启动客户端命令`log.io-file-input`

```
[root@localhost ~]# log.io-file-input 
[app1][192.168.1.140] Watching: /opt/logs/eureka.log
[app2][server1] Watching: /opt/saas-ws.log
[app1][192.168.1.140] Watching: /opt/base-ms.log
Connected to server: 192.168.1.141:6689
```

![](https://img-blog.csdnimg.cn/20210506164945650.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM5NjgwNTY0,size_16,color_FFFFFF,t_70)