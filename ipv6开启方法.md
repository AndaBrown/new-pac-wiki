**2018年3月15日增加teredo服务器地址。**

GoAgent ipv6版和GoProxy ipv6版需要电脑开启ipv6后才能使用，故出此教程。如果你试了各种方法还是开启不了IPV6，说明你那里的网络环境开启不了IPV6。翻墙软件除了两款IPV6版，还分享了很多其它不同类型的翻墙软件，比如GoProxy Quic版、SSR版、SkyZip版等，那么可以换其它类型的软件。

电脑系统开启ipv6的步骤如下：

1、打开控制面板---网络和共享中心--点本地连接---点属性---点tcp/IPv6----点属性---点使用下面的DNS服务器---在上面一行复制黏贴 2001:4860:4860::8888 下面一行复制黏贴 2001:4860:4860::8844 确定。如图：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-1.PNG)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-2.png)

上面这一组是google的ipv6 dns，如果不好用（不好用可以通过是否能成功开启ipv6的结果来判定），可以换下面这组ipv6 DNS ：

2620:0:ccc::2

2620:0:ccd::2

2、以管理员身份运行一键开启ipv6脚本

开启ipv6.bat [国外云盘1下载](http://45.32.141.248:8000/f/1679fb1b2d/?raw=1)  [国外云盘2下载](https://nofile.io/f/z6kjYEP42St/%E5%BC%80%E5%90%AFipv6.bat) 

关闭ipv6.bat  [国外云盘1下载](http://45.32.141.248:8000/f/6a0270b4eb/?raw=1) [国外云盘2下载](https://nofile.io/f/v1GCKWvgS9z/%E5%85%B3%E9%97%ADipv6.bat) 

右键选择“以管理员身份运行ipv6.bat文件后，需要等待3～5分钟才能设置好，如图如下：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/ipv6-13.PNG)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-4.PNG)

***

**注意：**

开启ipv6.bat脚本内置的是teredo的一个服务器，如果未来这个服务器被墙了或者不稳定，你都可以换备用的服务器来尝试，每一行代表一个服务器，如下：

win10.ipv6.microsoft.com

teredo2.remlab.net

win1710.ipv6.microsoft.com

teredo-debian.remlab.net

teredo.ginzado.ne.jp

teredo.iks-jena.de

teredo.ngix.ne.kr

teredo.autotrans.consulintel.com

teredo.managemydedi.com

teredo.trex.fi

debian-miredo.progsoc.org

替换方法：右键点击开启ipv6.bat，选择“编辑”，找到server=teredo.remlab.net （总共有两处相同的，都要替换！） ，将teredo.remlab.net替换成上面的其中1个服务器地址，保存后重新运行开启ipv6.bat文件。

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/ipv6/ipv6-102.PNG)

**2018年2月6日更新一键检测teredo服务器文件**：teredo-test-2018.2.6 [国外云盘1下载](http://45.32.141.248:8000/f/d13e465752/)   [国外云盘2下载](https://nofile.io/f/d1VmHY2XafZ/teredo-test-2018.2.6.rar) 
下载后解压出来，运行teredo.bat脚本，本脚本会批量检测teredo服务器的连通性，选择is accessible的服务器。因为teredo服务器比较多，当遇到ipv6被干扰严重的时候，使用一键检测脚本可以快速帮助用户知道目前哪个服务器连通性比较好，然后替换开启ipv6.bat脚本的默认服务器，提高方便性。（如果这个一键检测脚本不好用，那就手动一个一个的去替换服务器来尝试）

***

3、验证ipv6是否开启

打开 http://test-ipv6.com/ 网站，它会自动检测网络是否开启ipv6，如果开启了ipv6，会出现

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-5.PNG)

如果未开启，会出现

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-0.PNG)

**由于开启ipv6.bat脚本不是永久设置，所以重启后的电脑翻墙前需要再次运行ipv6脚本！**

***

如果上面的教程电脑系统不能开启ipv6，那么可以用微软的开启ipv6工具或者用下面的**其它方法**来尝试开启ipv6。 [微软开启ipv6工具下载页面](https://support.microsoft.com/zh-cn/help/929852/how-to-disable-ipv6-or-its-components-in-windows)  

1、如果“开启ipv6.bat”能测试成功，不用运行微软提供的启用 IPv6的工具。反之可以选择页面上的微软工具尝试开启IPv6，下载第二排最后1个，运行或者直接运行都可以。

2、如果ipv6能正常开启，将系统服务“IP Helper”设为“自动”，则重启电脑之后，ipv6应该是正常的，不用再运行“开启ipv6.bat”。

**其它方法**：

各操作系统情况不同，方法也不一样。

[IPv6-Win10](https://github.com/XX-net/XX-Net/wiki/IPv6-Win10)

[IPV6-Win7](https://github.com/XX-net/XX-Net/wiki/IPV6-Win7)

[IPv6-WinXP](https://github.com/XX-net/XX-Net/wiki/IPv6-WinXP)

[IPv6-Linux](https://github.com/XX-net/XX-Net/wiki/IPv6-Linux)

[IPv6-Mac](https://github.com/XX-net/XX-Net/wiki/IPv6-Mac)

[IPV6-路由器](https://github.com/XX-net/XX-Net/wiki/IPV6-%E8%B7%AF%E7%94%B1%E5%99%A8)

**注:如果你试了各种方法还是开启不了IPV6，说明你那里的网络环境开启不了IPV6。翻墙软件除了两款IPV6版，还分享了很多其它不同类型的翻墙软件，比如GoProxy Quic版、SSR版、SkyZip版等，那么可以换其它类型的软件。**

转载：[xx-net如何开启IPv6](https://github.com/XX-net/XX-Net/wiki/%E5%A6%82%E4%BD%95%E5%BC%80%E5%90%AFIPv6)  


***


如果有问题可以联系海外邮箱：kebi2014@gmail.com