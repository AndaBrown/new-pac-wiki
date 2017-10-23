电脑系统开启ipv6的步骤如下：

1、打开控制面板---网络和共享中心--点本地连接---点属性---点tcp/IPv6----点属性---点使用下面的DNS服务器---在上面一行复制黏贴 2001:4860:4860::8888 下面一行复制黏贴 2001:4860:4860::8844 ----确定。如图：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-1.PNG)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-2.PNG)


2、以管理员身份运行一键开启ipv6脚本

[一键开启ipv6脚本下载](https://nofile.io/f/aEFmQepaQhe/%E5%BC%80%E5%90%AFipv6.cmd)

[一键关闭ipv6脚本下载](https://nofile.io/f/fPaevSWGBGH/%E5%85%B3%E9%97%ADipv6.cmd)

右键选择“以管理员身份运行ipv6.cmd文件后，需要等待3～5分钟才能设置好，如图如下：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-3.png)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-4.PNG)

3、验证ipv6是否开启

打开http://test-ipv6.com/网站，它会自动检测网络是否开启ipv6，如果开启了ipv6，会出现

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-5.PNG)

如果未开启，会出现

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/goagent_ipv6/ipv6-0.PNG)

以上方法在win7旗舰版测试成功，如果你尝试了多次还是不行，那说明此方法不适合你的电脑系统。




