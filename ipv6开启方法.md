**2017年11月17日更新方法。GoAgent ipv6版和GoProxy ipv6版需要电脑开启ipv6后才能使用，故出此教程。**

电脑系统开启ipv6的步骤如下：

1、打开控制面板---网络和共享中心--点本地连接---点属性---点tcp/IPv6----点属性---点使用下面的DNS服务器---在上面一行复制黏贴 2001:4860:4860::8888 下面一行复制黏贴 2001:4860:4860::8844 ----确定。如图：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-1.PNG)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-2.png)

上面这一组是google的ipv6 dns，如果不好用（不好用可以通过是否能成功开启ipv6的结果来判定），可以换下面这组ipv6 DNS ：

2620:0:ccc::2

2620:0:ccd::2

2、以管理员身份运行一键开启ipv6脚本

开启ipv6.bat [国外云盘下载](https://nofile.io/f/z6kjYEP42St/%E5%BC%80%E5%90%AFipv6.bat) [本地下载](http://45.32.141.248:8000/f/1679fb1b2d/?raw=1)

关闭ipv6.bat [国外云盘下载](https://nofile.io/f/v1GCKWvgS9z/%E5%85%B3%E9%97%ADipv6.bat) [本地下载](http://45.32.141.248:8000/f/6a0270b4eb/?raw=1)

右键选择“以管理员身份运行ipv6.bat文件后，需要等待3～5分钟才能设置好，如图如下：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/ipv6-13.PNG)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-4.PNG)

**补充：**

开启ipv6.bat脚本内置的是teredo的一个服务器，如果未来这个服务器被墙了，可以换备用的服务器，每一行代表一个服务器，如下：

teredo2.remlab.net

teredo-debian.remlab.net

teredo.ginzado.ne.jp

teredo.iks-jena.de

teredo.ngix.ne.kr

teredo.autotrans.consulintel.com

teredo.managemydedi.com

替换方法：右键点击开启ipv6.bat，选择“编辑”，找到server=teredo.remlab.net ，将teredo.remlab.net替换成上面的其中1个服务器地址，保存即可。

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/ipv6/ipv6-100.PNG)



3、验证ipv6是否开启

打开 http://test-ipv6.com/ 网站，它会自动检测网络是否开启ipv6，如果开启了ipv6，会出现

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-5.PNG)

如果未开启，会出现

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-0.PNG)

**重启后的电脑翻墙前最好再次运行ipv6脚本，以确保IPv6被成功开启。**

***

**如果上面的教程电脑系统不能开启ipv6，那么可以用微软的开启ipv6工具。** [微软开启ipv6工具下载页面](https://support.microsoft.com/zh-cn/help/929852/how-to-disable-ipv6-or-its-components-in-windows)  

**补充**：

1、关于测试ipv6是否开启，还需要点击“测试项目”，“不使用域名的 IPv6 测试”这一项成功就肯定可以了。如下图:
![](https://raw.githubusercontent.com/abchb99/file/abchb99-patch-1/v6.jpg)

2、如果“开启ipv6.bat”能测试成功，不用运行微软提供的启用 IPv6的工具。反之可以选择页面上的微软工具“在所有隧道接口上重新启用 IPv6 ”尝试开启IPv6，下载如下图第1个和第5个，运行或者直接运行都可以。

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/ipv6/ipv6-2003.PNG)

3、如果ipv6能正常开启，将系统服务“IP Helper”设为“自动”，则重启电脑之后，ipv6应该是正常的，不用再运行“开启ipv6.bat”。


***


> 其它方法可参考：[xx-net](https://github.com/XX-net/XX-Net/wiki/%E5%A6%82%E4%BD%95%E5%BC%80%E5%90%AFIPv6)  [云栖社区](https://yq.aliyun.com/ziliao/27071)  


***


如果你有更好、更方便的方法，可以联系海外邮箱：kebi2014@gmail.com