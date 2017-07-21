**2017年7月21日更新制作PAC自动代理地址**

> 2017年7月10日更新代码为高匿名代码

> 2017年6月25日增加没有用户名和密码验证的PAC脚本代码

> 2017年6月22日更新加速教程

> 2017年6月6日更新一键部署PAC代码以及增加BBR加速脚本


***

教程很简单，整个教程分四步：

第一步：购买VPS服务器

第二步：一键部署VPS服务器

第三步：一键加速VPS服务器 （谷歌BBR加速或锐速加速；对速度要求不高的话，此步骤可省略）

第四步：实测


***
**第一步：购买VPS服务器**

VPS服务器需要选择国外的，首选国际知名的vultr，速度不错、稳定且性价比高。

vultr注册地址： http://www.vultr.com/?ref=7048874 （全球15个服务器位置可选，KVM框架。推荐买日本服务器，延迟低速度快。） 

虽然是英文界面，但是现在的浏览器都有网页翻译功能，鼠标点击右键，选择网页翻译即可翻译成中文。

注册并邮件激活账号，充值后即可购买服务器。充值方式是paypal，使用paypal有信用卡即可。paypal注册地址：https://www.paypal.com （paypal是国际知名的第三方支付服务商，相当于国内的支付宝。注册一下账号，绑定信用卡即可购买国外商品）

2.5美元/月的服务器配置信息：单核  512M内存  20G SSD硬盘   100M带宽   500G流量/月   

5美元/月的服务器配置信息：单核   1G内存   25G SSD硬盘   100M带宽    1000G流量/月  
 
10美元/月的服务器配置信息：单核  2G内存   40G SSD硬盘   100M带宽    2000G流量/月  


如图：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/paypal001.PNG)


购买vps服务器时，服务器地址优先选择：日本、新加坡（移动联通网络首选）；日本、洛杉矶、硅谷（电信网络首选）。**选择CentOS 6.X64位的系统（不要选择7以上的系统，很重要！7以上的系统会影响搭建以及下一步的锐速加速教程）**。完成购买后，找到系统的密码记下来，部署服务器时需要用到。如图：

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

链接成功后，会出现如上图所示，之后就可以输入代码部署成PAC了。

**部署代码有两种，一种是有用户名和密码验证的PAC脚本，另外一种是没有用户名和密码验证的PAC脚本。可根据自己需要选择。**

**有用户名和密码验证的PAC脚本代码如下：**

———————————————————代码分割线————————————————

setenforce 0

ulimit -n 800000

echo "* soft nofile 800000" >> /etc/security/limits.conf

echo "* hard nofile 800000" >> /etc/security/limits.conf

echo "alias net-pf-10 off" >> /etc/modprobe.d/dist.conf

echo "alias ipv6 off" >> /etc/modprobe.d/dist.conf

killall sendmail

/etc/init.d/postfix stop

chkconfig --level 2345 postfix off

chkconfig --level 2345 sendmail off

yum -y install squid wget

wget https://raw.githubusercontent.com/Alvin9999/PAC/master/centos-squid.conf -O /etc/squid/squid.conf

echo "root:W10fM8VWO04aM" >> /etc/squid/passwd

mkdir -p /var/cache/squid

chmod -R 777 /var/cache/squid

squid -z

service squid restart

chkconfig --level 2345 squid on

iptables -t nat -F

iptables -t nat -X

iptables -t nat -P PREROUTING ACCEPT

iptables -t nat -P POSTROUTING ACCEPT

iptables -t nat -P OUTPUT ACCEPT

iptables -t mangle -F

iptables -t mangle -X

iptables -t mangle -P PREROUTING ACCEPT

iptables -t mangle -P INPUT ACCEPT

iptables -t mangle -P FORWARD ACCEPT

iptables -t mangle -P OUTPUT ACCEPT

iptables -t mangle -P POSTROUTING ACCEPT

iptables -F

iptables -X

iptables -P FORWARD ACCEPT

iptables -P INPUT ACCEPT

iptables -P OUTPUT ACCEPT

iptables -t raw -F

iptables -t raw -X

iptables -t raw -P PREROUTING ACCEPT

iptables -t raw -P OUTPUT ACCEPT

service iptables save

———————————————————代码分割线————————————————


**没有用户名和密码验证的PAC脚本代码如下：**

———————————————————代码分割线————————————————

setenforce 0

ulimit -n 800000

echo "* soft nofile 800000" >> /etc/security/limits.conf

echo "* hard nofile 800000" >> /etc/security/limits.conf

echo "alias net-pf-10 off" >> /etc/modprobe.d/dist.conf

echo "alias ipv6 off" >> /etc/modprobe.d/dist.conf

killall sendmail

/etc/init.d/postfix stop

chkconfig --level 2345 postfix off

chkconfig --level 2345 sendmail off

yum -y install squid wget

wget https://raw.githubusercontent.com/Alvin9999/PAC/master/no-password.conf -O /etc/squid/squid.conf

mkdir -p /var/cache/squid

chmod -R 777 /var/cache/squid

squid -z

service squid restart

chkconfig --level 2345 squid on

iptables -t nat -F

iptables -t nat -X

iptables -t nat -P PREROUTING ACCEPT

iptables -t nat -P POSTROUTING ACCEPT

iptables -t nat -P OUTPUT ACCEPT

iptables -t mangle -F

iptables -t mangle -X

iptables -t mangle -P PREROUTING ACCEPT

iptables -t mangle -P INPUT ACCEPT

iptables -t mangle -P FORWARD ACCEPT

iptables -t mangle -P OUTPUT ACCEPT

iptables -t mangle -P POSTROUTING ACCEPT

iptables -F

iptables -X

iptables -P FORWARD ACCEPT

iptables -P INPUT ACCEPT

iptables -P OUTPUT ACCEPT

iptables -t raw -F

iptables -t raw -X

iptables -t raw -P PREROUTING ACCEPT

iptables -t raw -P OUTPUT ACCEPT

service iptables save

———————————————————代码分割线————————————————


**代码注意事项：如果你用的是vultr最低配置即2.5美元/月的服务器，当操作后没法正常使用，那么请将上述代码中的前三行数字800000改为稍小数字，然后再重新部署。**

将上面整个代码复制下来，鼠标右键即可。然后粘贴到到shell软件的命令栏里，之后就自动开始部署了，如果没有反应，敲键盘的“回车键”。部署成功标志如下：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell16.png)

注意上图两个带箭头的标志。

之后可以重启服务器确保部署生效，有时候不用重启也行。重启需要在命令栏里输入reboot。

注：上述指令中的这个指令 echo "root:W10fM8VWO04aM" >> /etc/squid/passwd 是将PAC代理的验证账号设定为默认帐号：root 密码：pac.itzmx.com。想设定其他账号的话可以用 http://tool.oschina.net/htpasswd 这个在线的htppasswd生成工具，加密算法选Crypt（All Unix Servers），如下图：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/006.png)

***

**第三步：一键加速VPS服务器**

此加速教程为谷歌BBR加速和破解版锐速加速教程，**两者只能成功装一个**，都仅支持KVM框架的vps服务器，vultr的服务器都是KVM框架。如果你购买的不是vultr的服务器，那么你需要搞清楚你买的vps服务器是否是KVM框架的，很重要。

按照第二步的步骤，重新连接服务器ip，登录成功后，在命令栏里粘贴以下代码：

【谷歌BBR加速教程】

yum -y install wget

wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh

chmod +x bbr.sh

./bbr.sh

把上面整个代码复制后粘贴进去，不动的时候按回车，然后耐心等待，最后重启vps服务器即可。该方法是开机自动启动，部署一次就可以了。

如图：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/bbr1.PNG)

出现上面这个图按回车

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/bbr2.PNG)

最后输入y重启服务器或者手动输入代码reboot

【锐速加速教程】

wget -N --no-check-certificate https://raw.githubusercontent.com/91yun/serverspeeder/master/serverspeeder-all.sh && bash serverspeeder-all.sh

把上面整个代码复制后粘贴进去。该方法是开机自动启动，部署一次就可以了。但有些内核是不适合的，部署过程中需要手动选择推荐的，当部署时出现以下字样：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/锐速2.PNG)

提示没有完全匹配的内核,随便选一个内核就行,按照提示来输入数字,按回车键即可

锐速安装成功标志如下：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/锐速3.png)

出现running字样即可!
***

**第四步：实测**

以我分享的谷歌浏览器PAC版为例：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/001.png)

依次打开浏览器地址栏右边的代理扩展按钮，打开选项

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/002.png)

先选择右边的新建情景模式，然后再弹出的对话框中，输入名称（随便取），情景模式类型为第一个的代理服务器。然后点击创建


![](https://raw.githubusercontent.com/Alvin9999/PAC/master/005.png)

代理协议为http ，服务器填你的vps服务器ip，代理端口选择25 。然后输入用户名和密码。最后点击右侧绿色的应用选项使设置生效。这样设置的话，就是全局代理了，即所有的网站都通过国外代理。

然后你选中你的PAC地址，试试能不能翻出去以及翻墙速度如何就可以了。整个教程，第二步很关键，通常第二步完成后，在加速前就可以先实测一下是否部署成功。

***

**制作PAC自动代理地址教程（可选）**：

上面的教程翻墙够用了，但有的人希望制作PAC自动代理地址，即国内网站不走代理，国外需要翻墙的网站才走代理，故出此教程。本教程需要在
 https://github.com 网站注册一个账号，且创建一个项目，如果未来这个github网站被墙了，相应的该方法也会随之失效，提醒下。

例如，我创建了一个名字叫“PAC”的项目，且在这个项目下创建一个文件，这里取名为“pac001”

那么对应的PAC代理地址为：https://raw.githubusercontent.com/Alvin9999/PAC/master/pac001

你创建了文件后，用浏览器打开上面的代理地址，把整个内容复制到文件中，然后把你的vps服务器ip替换原先的“你的vps服务器ip”，之后提交保存。

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/pac地址001.png)


这样PAC地址就制作成了，具体的PAC地址格式可以参考https://raw.githubusercontent.com/Alvin9999/PAC/master/pac001 ，**Alvin9999**改成你的github的用户名，**PAC**改成你创建的项目名称，**pac001**改成你的项目下创建的文件名称。

例如：https://raw.githubusercontent.com/张三/项目名/master/文件名  （可以用浏览器打开自己制作的地址，如果能正常打开且能看到内容说明地址没错，看不到内容证明写错了，好好检查下）

制作完地址后，使用谷歌浏览器的SwitchyOmega扩展，创建情景模式就能使用PAC代理地址

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/pac地址002.png)

创建后复制自己的地址进去，然后点击**立即更新情景模式**

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/pac地址003.png)


最后，选中自己的PAC地址就能自动代理上网。

***

### 鸣谢：[小樱](http://bbs.itzmx.com/thread-8815-1-1.html) [91yun](https://www.91yun.org/archives/683)  [秋水逸冰](https://teddysun.com/489.html)


***

有问题请发邮件到kebi2014@gmail.com 



