> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [baijiahao.baidu.com](https://baijiahao.baidu.com/s?id=1714641263988021723&wfr=spider&for=pc) 如何在 Ubuntu 中安装 Node.js播报文章[![](https://gips0.baidu.com/it/u=2134610665,162947751&fm=3012&app=3012&autime=1667780241&size=b200,200)](https://author.baidu.com/home?from=bjh_article&app_id=1711489012880566)[

苗子说全栈

](https://author.baidu.com/home?from=bjh_article&app_id=1711489012880566)2021-10-26 08:49关注

在上一章中， 我们说了 Mac 中安装 Node.js 这节主要来说一下， 在 Ubuntu 中如何进行安装 Node.js  

官方下载网站： [https://nodejs.org/zh-cn/download/](javascript:void(0))

使用版本是： 14.18.1  

安装方式使用：  

*   软件包安装（应用商店安装）
    
*   包管理器安装  
    

### Linux 安装篇

这里使用 Ubuntu Desktop 的版本进行安装演示。其他的操作系统和这三种基本上差不多。

### 软件包安装

使用 Ubuntu Software 安装， 打开 Ubuntu Software：

![](https://pics6.baidu.com/feed/6d81800a19d8bc3e8a095a3334e7f517a9d345bf.png@f_auto?token=a9f734a4e8b866719f25cb1d6cac931e)

点击 Node.js

![](https://pics3.baidu.com/feed/d8f9d72a6059252d624db95883f750325ab5b98e.png@f_auto?token=ed500e793760a10d010ece4959d7ef1e)

点击 **安装** 等着安装就可以了。 安装完成进行测试即可。

### 软件包管理器安装

ubuntu 的默认管理器是 apt-get 进行安装。

首先指定安装源， 这样是安装 14.x 的版本。

```
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
```

也可以使用最新版本, 当前是 16.x 的版本。 这里我使用了 LTS 版本。

```
curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash -
```

接着安装 Node.js

```
sudo apt-get install nodejs
```

可以默认同意安装加上 `-y`

```
sudo apt-get install -y nodejs
```

![](https://pics1.baidu.com/feed/0823dd54564e92580cd40d4e2aee8251cdbf4e20.png@f_auto?token=2994b6e6e908d6c8db4d7fbc71c9ce50)

最后没有错误， 就说明安装完成， 使用 node -v 和 npm -v 进行测试。显示版本号， 安装完成。

安装结束。准备开始燥起来吧。继续学习。 关注我。后续更多内容呈现中。

举报 / 反馈大家都在搜[ubuntu 安装 nodejs](https://baidu.com/s?word=ubuntu%E5%AE%89%E8%A3%85nodejs&rsv_dl=feed_landingpage_rs&from=1020853i&rsf= "ubuntu安装nodejs")[ubuntu 一键安装依赖包](https://baidu.com/s?word=ubuntu%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E4%BE%9D%E8%B5%96%E5%8C%85&rsv_dl=feed_landingpage_rs&from=1020853i&rsf= "ubuntu一键安装依赖包") [ubuntu source](https://baidu.com/s?word=ubuntu%20source&rsv_dl=feed_landingpage_rs&from=1020853i&rsf= "ubuntu source")[ubuntu source 命令](https://baidu.com/s?word=ubuntu%20source%E5%91%BD%E4%BB%A4&rsv_dl=feed_landingpage_rs&from=1020853i&rsf= "ubuntu source命令") [nodejs gui](https://baidu.com/s?word=nodejs%20gui&rsv_dl=feed_landingpage_rs&from=1020853i&rsf= "nodejs gui")[ubuntu 安装教程 18.04](https://baidu.com/s?word=ubuntu%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B18.04&rsv_dl=feed_landingpage_rs&from=1020853i&rsf= "ubuntu安装教程18.04")

发表评论
----

发表

作者最新文章
------

![](https://t12.baidu.com/it/app=106&f=JPEG&fm=30&fmt=auto&u=3922009075%2C189474587?w=660&h=371&s=28A47C32138F4149485560DE0300C0B2)[

### Gradle 构建 Spring Boot 项目

](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_8742936006982548445%22%7D&n_type=1&p_from=3)2 天前 86 阅读![](https://t10.baidu.com/it/app=106&f=JPEG&fm=30&fmt=auto&u=3088578134%2C189366025?w=375&h=210&s=69C29345C2FC9C6D1C742423030080C2)[

### MyBatis 的查询映射器 select 使用方式大全 2

](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_9423865933445636925%22%7D&n_type=1&p_from=3)4 天前 5 阅读![](https://t10.baidu.com/it/app=106&f=JPEG&fm=30&fmt=auto&u=2596408355%2C189290056?w=660&h=371&s=341E6C32595FD1C85EF451DE0300C0B1)[

### MyBatis 的查询映射器 select 使用方式大全 1

](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_9770557746657745053%22%7D&n_type=1&p_from=3)5 天前 12 阅读

相关推荐
----

![](https://t11.baidu.com/it/app=106&f=JPEG&fm=30&fmt=auto&u=3161958503%2C189709046?w=312&h=208&s=7F1EF3AE8C1263E7C404581A0300D070)[

### 微软 Linux Windows 子系统获得重要进展，Windows10 用户可用

](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_10352294368068912176%22%7D&n_type=1&p_from=4)[互联范儿](https://author.baidu.com/home?from=bjh_article&app_id=1547591810390121) [1 评论](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_10352294368068912176%22%7D&n_type=1&p_from=4)![](https://t10.baidu.com/it/app=106&f=JPEG&fm=30&fmt=auto&u=3729966352%2C189644230?w=312&h=208&s=73D4778E5BE8856A4C5DF5070300F047)[

### 如何重装永久版 Office 家庭和学生版 2021

](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_8950235923540896993%22%7D&n_type=1&p_from=4)[华硕服务](https://author.baidu.com/home?from=bjh_article&app_id=1607470576613977)[](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_8950235923540896993%22%7D&n_type=1&p_from=4)![](https://t12.baidu.com/it/app=106&f=JPEG&fm=30&fmt=auto&u=1166635558%2C189628297?w=312&h=208&s=A9126195D2218EF4DC1DCC8D03002081)[

### MariaDB 10.11 将作为 LTS 版本提供

](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_9209814280922247397%22%7D&n_type=1&p_from=4)[开源中国](https://author.baidu.com/home?from=bjh_article&app_id=1653861004982757)[](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_9209814280922247397%22%7D&n_type=1&p_from=4)![](https://t11.baidu.com/it/app=106&f=JPEG&fm=30&fmt=auto&u=2749178352%2C189708523?w=312&h=208&s=7294A52A958B414B12C1497C0300C033)[

### 早期项目｜对标 40 亿美金 Webflow，「Towify」想用无代码方式搭建小程序

](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_9659397460189859597%22%7D&n_type=1&p_from=4)[36 氪](https://author.baidu.com/home?from=bjh_article&app_id=1566365578755720)[](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_9659397460189859597%22%7D&n_type=1&p_from=4)![](https://t10.baidu.com/it/app=106&f=JPEG&fm=30&fmt=auto&u=2713566069%2C189617544?w=312&h=208&s=1889B95E5BA5B97A0EE254830300B088)[

### 微软在 Win11 build 25247 开始菜单中塞入推荐网站，教你如何去掉

](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_8856991706847740276%22%7D&n_type=1&p_from=4)[IT 之家](https://author.baidu.com/home?from=bjh_article&app_id=1551599273641720)[](https://mbd.baidu.com/newspage/data/landingsuper?context=%7B%22nid%22%3A%22news_8856991706847740276%22%7D&n_type=1&p_from=4)[](https://top.baidu.com/board?platform=pc&sa=pcindex_entry)换一换

*   1[31 省份新增本土 3927+27517](https://www.baidu.com/s?wd=31%E7%9C%81%E4%BB%BD%E6%96%B0%E5%A2%9E%E6%9C%AC%E5%9C%9F3927%2B27517&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc) 热

*   2[C 罗和内马尔今日登场](https://www.baidu.com/s?wd=C%E7%BD%97%E5%92%8C%E5%86%85%E9%A9%AC%E5%B0%94%E4%BB%8A%E6%97%A5%E7%99%BB%E5%9C%BA&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc)热

*   3 [卡塔尔世界杯中国元素抢眼](https://www.baidu.com/s?wd=%E5%8D%A1%E5%A1%94%E5%B0%94%E4%B8%96%E7%95%8C%E6%9D%AF%E4%B8%AD%E5%9B%BD%E5%85%83%E7%B4%A0%E6%8A%A2%E7%9C%BC&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc)

*   4 [孙兴慜将戴面具出战乌拉圭](https://www.baidu.com/s?wd=%E5%AD%99%E5%85%B4%E6%85%9C%E5%B0%86%E6%88%B4%E9%9D%A2%E5%85%B7%E5%87%BA%E6%88%98%E4%B9%8C%E6%8B%89%E5%9C%AD&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc)

*   5 [被赌球毁掉的干部 有人欠债近 2000 万](https://www.baidu.com/s?wd=%E8%A2%AB%E8%B5%8C%E7%90%83%E6%AF%81%E6%8E%89%E7%9A%84%E5%B9%B2%E9%83%A8+%E6%9C%89%E4%BA%BA%E6%AC%A0%E5%80%BA%E8%BF%912000%E4%B8%87&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc)

*   6[FIFA 点赞日本队：更衣室一尘不染](https://www.baidu.com/s?wd=FIFA%E7%82%B9%E8%B5%9E%E6%97%A5%E6%9C%AC%E9%98%9F%EF%BC%9A%E6%9B%B4%E8%A1%A3%E5%AE%A4%E4%B8%80%E5%B0%98%E4%B8%8D%E6%9F%93&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc)

*   7 [北京新增 1 例死亡病例](https://www.baidu.com/s?wd=%E5%8C%97%E4%BA%AC%E6%96%B0%E5%A2%9E1%E4%BE%8B%E6%AD%BB%E4%BA%A1%E7%97%85%E4%BE%8B&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc)

*   8 [四川健康码崩了 官方回应](https://www.baidu.com/s?wd=%E5%9B%9B%E5%B7%9D%E5%81%A5%E5%BA%B7%E7%A0%81%E5%B4%A9%E4%BA%86+%E5%AE%98%E6%96%B9%E5%9B%9E%E5%BA%94&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc)

*   9 [女教师上网课时遭家暴 警方回应](https://www.baidu.com/s?wd=%E5%A5%B3%E6%95%99%E5%B8%88%E4%B8%8A%E7%BD%91%E8%AF%BE%E6%97%B6%E9%81%AD%E5%AE%B6%E6%9A%B4+%E8%AD%A6%E6%96%B9%E5%9B%9E%E5%BA%94&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc)

*   10 [建站 63 年来第一次闭站？北京站辟谣](https://www.baidu.com/s?wd=%E5%BB%BA%E7%AB%9963%E5%B9%B4%E6%9D%A5%E7%AC%AC%E4%B8%80%E6%AC%A1%E9%97%AD%E7%AB%99%EF%BC%9F%E5%8C%97%E4%BA%AC%E7%AB%99%E8%BE%9F%E8%B0%A3&sa=fyb_news_feedpc&rsv_dl=fyb_news_feedpc&from=feedpc)