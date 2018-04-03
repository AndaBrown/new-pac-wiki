**2018年4月2日更新一键配置ipv6.bat脚本。**

***

**电脑系统开启ipv6的步骤如下：**

1、打开控制面板---网络和共享中心--点本地连接---点属性---点tcp/IPv6----点属性---点使用下面的DNS服务器---在上面一行复制黏贴 2001:4860:4860::8888 下面一行复制黏贴 2001:4860:4860::8844 确定。如图：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-1.PNG)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-2.png)

上面这一组是google的ipv6 dns，如果不好用（不好用可以通过是否能成功开启ipv6的结果来判定），可以换下面这组ipv6 DNS ：

2620:0:ccc::2

2620:0:ccd::2

2、以管理员身份运行一键**配置ipv6.bat**脚本

配置ipv6.bat  [国外云盘1下载](http://45.32.141.248:8000/f/06b0039dab/?raw=1) [国外云盘2下载](http://108.61.224.82:8000/f/b246dea5b8/?raw=1) [国外云盘3下载](https://nofile.io/f/SbesKuddq25/%E9%85%8D%E7%BD%AEIPv6.bat) [国内云盘下载](https://pan.baidu.com/s/1dJFdMZiSkfAK7XsTzUdtSQ)

关闭ipv6.bat  [国外云盘1下载](http://45.32.141.248:8000/f/6a0270b4eb/?raw=1) [国外云盘2下载](https://nofile.io/f/v1GCKWvgS9z/%E5%85%B3%E9%97%ADipv6.bat) 

右键选择“以管理员身份运行**配置ipv6.bat**文件

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/softimag/new-ipv6-0.PNG)

**之后会出现以下界面：**

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/softimag/new-ipv6-1.PNG)

**输入数字1来手动设置Teredo服务器，敲回车键会出现以下界面：**

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/softimag/new-ipv6-2.PNG)

**脚本内置11个Teredo服务器，一次选1个服务器即可，可以从上往下依次测试。输入Teredo服务器对应前面的数字，之后敲回车键，耐心等待30秒～2分钟，会出现以下界面：**

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/softimag/new-ipv6-3.PNG)

**当界面出现“操作完成”，脚本会自动返回主界面**

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/softimag/new-ipv6-4.PNG)

**输入数字2，查看Teredo隧道状态，当服务器名称是你手动设置的Teredo服务器名称表明设置成功**

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/softimag/new-ipv6-6.PNG)

**之后，关掉脚本，30秒之后打开对应软件版本的一键启动程序启动翻墙插件和浏览器，如果用浏览器能成功翻墙，表明你选择的Teredo服务器在你所在地区处于可用状态，如果不能翻墙，表明你选择的Teredo服务器被封锁，那么请重复上面的步骤更换Teredo服务器。如果所有的Teredo服务器都尝试了，但还是不能翻墙，说明你所在地区Teredo隧道被完全封锁，至少目前是这样，至于以后会不会解封处于未知状态，此时最好的办法就是更换其它类型的软件。**

**注意：当电脑重启后，需要重新设置Teredo服务器，因为本脚本不是永久设置！**

***


**其它开启ipv6方法**：

各操作系统情况不同，方法也不一样。

[IPv6-Win10](https://github.com/XX-net/XX-Net/wiki/IPv6-Win10)

[IPV6-Win7](https://github.com/XX-net/XX-Net/wiki/IPV6-Win7)

[IPv6-WinXP](https://github.com/XX-net/XX-Net/wiki/IPv6-WinXP)

[IPv6-Linux](https://github.com/XX-net/XX-Net/wiki/IPv6-Linux)

[IPv6-Mac](https://github.com/XX-net/XX-Net/wiki/IPv6-Mac)

[IPV6-路由器](https://github.com/XX-net/XX-Net/wiki/IPV6-%E8%B7%AF%E7%94%B1%E5%99%A8)

**注:如果你试了各种方法还是开启不了IPV6，说明你那里的网络环境开启不了IPV6。那么可以换其它类型的软件，比如GoProxy Quic版、v2ray版、SSR版、SkyZip版等。**

转载：[xx-net如何开启IPv6](https://github.com/XX-net/XX-Net/wiki/%E5%A6%82%E4%BD%95%E5%BC%80%E5%90%AFIPv6)  


***


如果有问题可以联系海外邮箱：kebi2014@gmail.com