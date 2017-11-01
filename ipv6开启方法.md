**2017年11月1日更新，增加微软开启ipv6工具。**

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

3、验证ipv6是否开启

打开 http://test-ipv6.com/ 网站，它会自动检测网络是否开启ipv6，如果开启了ipv6，会出现

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-5.PNG)

如果未开启，会出现

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-0.PNG)

**重启后的电脑翻墙前最好再次运行ipv6脚本，以确保IPv6被成功开启。**

以上方法在win7旗舰版测试成功，如果你尝试了两次还是不行，可以用**微软提供的一些启用IPv6的工具** [微软下载地址页面](https://support.microsoft.com/zh-cn/help/929852/how-to-disable-ipv6-or-its-components-in-windows)


***


> 其它方法可参考：https://yq.aliyun.com/ziliao/27071

https://github.com/XX-net/XX-Net/wiki/%E5%A6%82%E4%BD%95%E5%BC%80%E5%90%AFIPv6


如果你有更好的方法，可以联系海外邮箱：kebi2014@gmail.com