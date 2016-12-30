**2016年12月30日更新**

教程很简单，整个教程分三步：

第一步：购买VPS服务器

第二步：一键部署VPS服务器

第三步：一键加速VPS服务器 （对速度要求不高的话，此步骤可省略）


***
**第一步：购买VPS服务器**

VPS服务器需要选择国外的，首选国际知名的vultr，速度不错且很稳定。用此链接注册http://www.vultr.com/?ref=7052665-3B （**促销中，新用户账号可获得20美元奖励资金，奖励资金没法提现，只能用于购买服务器**），vps服务器最低配置是5美元/月（实际是按照小时计费的），每月流量1000G，个人用完全够了。虽然是英文界面，但是现在的浏览器都有网页翻译功能，鼠标点击右键，选择网页翻译即可翻译成中文。

5美元/月的服务器配置信息：单核   768M内存   15G SSD硬盘   1G带宽    1000G流量    

注册并邮件激活账号后，需要首次充值最低5美元，方可获得20美元的优惠奖励。方式是信用卡或者采用全球付的paypal，如果没有信用卡，可以用paypal，因为paypal可以支持银联卡，不仅是信用卡。注册paypal很简单（网站：paypal.com），这里就不弄教程了，百度或者google一下就有了。如图：

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程00.png)


购买vps服务器时，服务器地址优先选择：**日本、新加坡（移动联通网络首选）；洛杉矶、硅谷（电信网络首选）**。选择**CentOS 6.X64**位的系统（不要选择7以上的系统）。完成购买后，找到系统的密码记下来，部署服务器时需要用到。如图：

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程01.png)

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程02.png)

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程04.png)

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程05.png)

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程06.png)

上图是我选择的10美元/月的日本服务器，加速后，不同的网络类型效果不完全相同，移动联通网络很快，电信也还行。电信网络用户还可以选择美国西海岸的服务器，比如洛杉矶或者硅谷。因为vultr实际上是折算成小时来计费的，所以如果你部署的服务器实测后不理想，你可以把它删掉，重新换个地区的服务器来部署，很方便。


***
**第二步：部署VPS服务器**

购买服务器后，需要部署一下。因为你买的是虚拟东西，而且又远在国外，我们需要一个叫Xshell的软件来远程部署。Xshell下载地址：

MEGA网盘：https://mega.nz/#!JxpiWLbA!yOoK5vmxaVnpl-rbyJQKxU3hSXnAHcMDp_sEJA5uDy0 （翻墙打开此下载地址会更快）

百度软件中心：http://rj.baidu.com/soft/detail/15201.html?ald

***

部署教程：

下载xshell软件并安装后，打开软件

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell11.png)

选择文件，新建

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell12.png)

随便取个名字，然后把你的服务器ip填上

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell13.png)

连接国外ip即服务器时，软件会先后提醒你输入用户名和密码，用户名linus系统默认都是root，密码是购买服务器后的cent系统的密码。
![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell14.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell15.png)

链接成功后，会出现如上图所示，之后就可以输入代码部署成ss了。

一键部署ss代码如下：

———————————————————代码分割线————————————————

wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev.sh
chmod +x shadowsocks-libev.sh

./shadowsocks-libev.sh 2>&1 | tee shadowsocks-libev.log


———————————————————代码分割线————————————————

将上面整个代码复制下来，鼠标右键即可。然后粘贴到到shell软件的命令栏里，之后就自动开始部署了。

运行后，首先会提示你设置密码，以12345678为例，输入密码后，敲回车键，如图：

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/ss1.png)

其次，会提示你输入ss的端口号，以8888为例，如图：

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/ss2.png)

然后，按任意键继续部署

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/ss3.png)


耐心等待，最后部署成功标志如下：

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/ss4.png)


之后可以重启服务器确保部署生效，有时候不用重启也行。重启需要在命令栏里输入reboot。如果部署失败，卡在某个位置，可以用xshell软件断开，然后重新连接你的ip，再复制代码进行部署

***

**第三步：一键加速VPS服务器**

此加速教程为破解版锐速加速教程，但仅支持KVM框架的vps服务器，vultr的服务器都是KVM框架。如果你购买的不是vultr的服务器，那么你需要搞清楚你买的vps服务器是否是KVM框架的，很重要。

按照第二步的步骤，重新连接服务器ip，登录成功后，在命令栏里粘贴以下代码：

wget -N --no-check-certificate https://raw.githubusercontent.com/91yun/serverspeeder/master/serverspeeder-all.sh && bash serverspeeder-all.sh

如果嫌速度太快，受不了，可以选择卸载加速（可能性不大）。卸载一键加速代码命令为：

chattr -i /serverspeeder/etc/apx* && /serverspeeder/bin/serverSpeeder.sh uninstall -f

该方法是开机自动启动，部署一次就可以了。但有些内核是不适合的，部署过程中需要手动选择推荐的，当部署时出现以下字样：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/锐速2.PNG)

提示没有完全匹配的内核,随便选一个内核就行,按照提示来输入数字,按回车键即可

锐速安装成功标志如下：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/锐速3.png)

出现running字样即可!


***



有问题请发邮件到kebi2014@gmail.com 
