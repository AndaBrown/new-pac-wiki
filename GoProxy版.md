
**最近更新内容：**

**2017年6月28日升级GoProxy至1454版，同时开启Quic协议。更新后可用ip数大幅度增加。由于目前Quic协议还不完善，所以如果你用此版发现不好用，可以运行ip更新文件来关闭Quic协议。**

> 2017年6月26日云端更新900+高质量谷歌ip

> 2017年6月14日云端更新设置，解决YouTube首页无法打开的问题，旧版用户按照使用说明运行ip更新文件即可同步，之后必须升级浏览器内核为53版本才能生效。注意：如果你的电脑是win7及以上系统，下载完整版，先按照内核升级方法升级浏览器内核至53版本，然后运行ip更新文件，两者缺一不可。其次，你还可以用刚发布的[谷歌浏览器59内核便携版](https://github.com/Alvin9999/new-pac/wiki/%E9%AB%98%E5%86%85%E6%A0%B8%E4%BE%BF%E6%90%BA%E7%89%88)。 

> 如果你的电脑是xp系统，因为XP系统最高只能用49内核，根据反馈和测试，目前用GoAgent版和GoProxy版升级到49内核后不能成功打开YouTube。鉴于此，有两个建议：一、换电脑系统为win7或以上系统；二、如果不换系统的话，可以换其它版本的软件，比如谷歌浏览器PAC版或GOGO翻墙软件等，又或者[火狐浏览器便携版](https://github.com/Alvin9999/new-pac/wiki/%E7%81%AB%E7%8B%90%E6%B5%8F%E8%A7%88%E5%99%A8%EF%BC%88GoAgent%E3%80%81GoProxy%E5%92%8CLantern%E7%89%88%EF%BC%89)。

> 2017年5月28日云端更新500+高质量ip

> 2017年5月23日更新GoProxy版本至r1412，运行更流畅

***

### 低内核完整版 （适合windows系统，包括xp）

压缩包名称Chrome53_gop_v2017.6.28.7z ，文件大小149.53M。压缩包里的ChromeUpdate文件夹有两个内核离线包(Xp系统49内核和win7及以上系统53内核），共计86M。

**下载地址：**

[巴别鸟云盘下载](http://www.babel.cc/share.do?s=2539182178850811) 提取密码：50283

[盛天云盘下载](http://pan.stnts.com/s/f6sLpKe) 

[百度云网盘下载](http://pan.baidu.com/s/1c1IA6L6) 密码：53re（第一次打开时如果出现提示百度云升级，页面不存在等，刷新一下网页）

**注意：启动后如果发现good_addrs=0且几分钟后都加载不出来，或者网站刚开始能打开之后不能打开，遇到这些情况重新启动GoProxy，一般1～3次。这是由于GoProxy还不完善的原因所导致的，需要时间。**


***

使用方法：下载后解压，按文件夹里面的使用说明（必看）操作。

***

**自动更新GoProxy版本号方法：** 

打开Agent文件夹，找到get-latest-goproxy.cmd文件，右键它选择“以管理员身份运行”

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/自动版本1.png)

服务器会自动从github上下载最新的goproxy版本，当新版本比当前版本高时，会自动下载和替换，一般2～5分钟

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/自动版本2.png)

通常1～2周运行一次get-latest-goproxy.cmd文件，只要是开发者更新了就能同步更新。

如果你等了很久没有更新成功，也运行了很多次，那说明该更新地址在你那里被屏蔽了，你也不用太担心，因为我每隔一段时间会手动更新版本，到时候下载我更新后的压缩包就行。

***

低内核完整版实例图

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent综合版使用1.png)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/GOP1.png)

***

有问题可以来信交流kebi2014@gmail.com