**教程很简单，整个教程分三步**：

第一步：购买VPS服务器

第二步：一键部署VPS服务器

第三步：一键加速VPS服务器 （对速度要求不高的话，此步骤可省略）


***
**第一步：购买VPS服务器**

VPS服务器需要选择国外的，首选国际知名的vultr，速度不错、稳定且性价比高。vultr注册地址：https://www.vultr.com/match （全球15个服务器位置可选，KVM框架，新账号冲多少送多少，最高送100美元） 虽然是英文界面，但是现在的浏览器都有网页翻译功能，鼠标点击右键，选择网页翻译即可翻译成中文。

注册并邮件激活账号，充值后即可购买服务器。充值方式是信用卡或者采用全球付的paypal，如果没有信用卡或者信用卡支付失败，可以用paypal代付。paypal官网地址：https://www.paypal.com （paypal是国际知名的第三方支付服务商，相当于国内的支付宝。注册一下账号，绑定信用卡或者银联卡即可购买国外商品）

5美元/月的服务器配置信息：单核   1G内存   25G SSD硬盘   100M带宽    1000G流量/月  
 
10美元/月的服务器配置信息：单核  2G内存   40G SSD硬盘   100M带宽    2000G流量/月  

如图：

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程00.png)


购买vps服务器时，服务器地址优先选择：日本、新加坡（移动联通网络首选）；洛杉矶、硅谷（电信网络首选）。**选择CentOS 6.X64位的系统（不要选择7以上的系统，很重要！7以上的系统会影响搭建以及下一步的锐速加速教程）**。完成购买后，找到系统的密码记下来，部署服务器时需要用到。如图：

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程01.png)

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程02.png)

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程04.png)

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程05.png)

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程06.png)

因为vultr实际上是折算成小时来计费的，所以如果你部署的服务器实测后不理想，你可以把它删掉，重新换个地区的服务器来部署，很方便。


***
**第二步：部署VPS服务器**

购买服务器后，需要部署一下。因为你买的是虚拟东西，而且又远在国外，我们需要一个叫Xshell的软件来远程部署。Xshell下载地址：

[巴别鸟云盘下载](http://www.babel.cc/share.do?s=5793540665720793) 提取密码：38693

[MEGA云盘下载](https://mega.nz/#!JxpiWLbA!yOoK5vmxaVnpl-rbyJQKxU3hSXnAHcMDp_sEJA5uDy0) （翻墙打开）

[百度软件中心](http://rj.baidu.com/soft/detail/15201.html?ald)

***

部署教程：

下载xshell软件并安装后，打开软件

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell11.png)

选择文件，新建

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell12.png)

随便取个名字，然后把你的服务器ip填上

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell13.png)

连接国外ip即服务器时，软件会先后提醒你输入用户名和密码，用户名linux系统默认都是root，密码是购买服务器后的cent系统的密码。
![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell14.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell15.png)

链接成功后，会出现如上图所示，之后就可以输入代码部署成ss了。

一键部署ss代码（适用于：CentOS 6&7）如下：

———————————————————代码分割线————————————————

yum -y install wget

wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev.sh

chmod +x shadowsocks-libev.sh

./shadowsocks-libev.sh 2>&1 | tee shadowsocks-libev.log

———————————————————代码分割线————————————————

一键部署ssR代码(支持混淆协议）如下：

wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh

chmod +x shadowsocksR.sh

./shadowsocksR.sh 2>&1 | tee shadowsocksR.log

———————————————————代码分割线————————————————

根据需求选择SS代码或SSR代码，然后将代码复制下来，鼠标右键即可。然后粘贴到到shell软件的命令栏里，之后就自动开始部署了，如果没有反应，敲键盘的“回车键”。

以SS代码运行为例，首先会提示你设置密码，以12345678为例，输入密码后，敲回车键，如图：

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

如果嫌速度太快，受不了，可以选择卸载加速。卸载一键加速代码命令为：

chattr -i /serverspeeder/etc/apx* && /serverspeeder/bin/serverSpeeder.sh uninstall -f

该方法是开机自动启动，部署一次就可以了。但有些内核是不适合的，部署过程中需要手动选择推荐的，当部署时出现以下字样：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/锐速2.PNG)

提示没有完全匹配的内核,随便选一个内核就行,按照提示来输入数字,按回车键即可

锐速安装成功标志如下：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/锐速3.png)

出现running字样即可!

***

**如果你部署的ss服务器只是自己用，可以不用看下面的教程。下面的教程主要是针对愿意将ss账号分享给别人使用时，可供参考的其它脚本。**


***

附：

**一个简单的防DDOS脚本**

**安装：**

wget http://www.inetbase.com/scripts/ddos/install.sh

chmod +x install.sh

./install.sh

**卸载：**

wget http://www.inetbase.com/scripts/ddos/uninstall.sh

chmod +x uninstall.sh

./uninstall.sh

原理：用Cron计划任务定时执行脚本统计单个IP的最大连接数，如果超过阈值则用APF活着iptables来阻止，并在预设的阻止时间后释放。


***

**CentOS上封邮件发出实现防SPAM和BT、PT的教程**，代码如下：

wget -4qO- onekey.sh/Get_Out_Spam|bash

***

### 鸣谢：[秋水逸冰](https://teddysun.com/392.html) [91yun](https://www.91yun.org/archives/683)  [张朝权博客](https://www.zhangchaoquan.com/index.php/linux/219.html) [时刻知](http://www.shikezhi.com/html/2016/linux_1004/1227496.html)


***

上面的教程很详细了，如果在搭建过程中，还遇到一些搞不懂的地方，可以用google搜索，只要是网上有的，基本上都能搜到。如果你没有搜到，不妨试着优化一下关键词。或者有问题你也可以发邮件到kebi2014@gmail.com 
