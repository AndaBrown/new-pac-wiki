**2020年9月4日更新脚本。**

**如果无法查看图片，可以访问https://tr1.freeair888.club/自建v2ray服务器教程**

***

**自建v2ray教程很简单，整个教程分三步**：

第一步：购买VPS服务器 

第二步：一键部署VPS服务器

第三步：一键加速VPS服务器 （五合一的TCP网络加速脚本）

***

**【前言】**

**v2ray的优势**：v2ray支持的传输方式有很多，包括：普通TCP、HTTP伪装、WebSocket流量、普通mKCP、mKCP伪装FaceTime通话、mKCP伪装BT下载流量、mKCP伪装微信视频流量，不同的传输方式其效果会不同，有可能会遇到意想不到的效果哦！当然国内不同的地区、不同的网络环境，效果也会不同，所以具体可以自己进行测试。现在v2ray客户端也很多了，有windows、MAC、linux和安卓版。

***

**第一步：购买VPS服务器**

VPS服务器需要选择国外的，首选国际知名的vultr，速度不错、稳定且性价比高，按小时计费，能够随时开通和删除服务器，新服务器即是新ip。

vultr活动地址：https://www.vultr.com/?ref=8418982-6G （vutr活动，新用户注册送100美元，vps最低2.5美元/月，vultr全球17个服务器位置可选，新增韩国服务器。支持支付宝和paypal付款。） 

vultr活动注意：只针对从没有注册过vultr产品的用户，都可以收到来自vultr官方赠送的100美元的试用金额。不过，用户必须使用信用卡或者PayPal来激活；试用期为1个月，没有使用完的额度会自动失效！官方除了支持PayPal和信用卡付款之外，还支持支付宝、比特币，不过你使用这些付款的话就不能享受100美元的试用金额了。

<a href="https://www.vultr.com/?ref=8418982-6G"><img src="https://www.vultr.com/media/banners/banner_728x90.png" width="728" height="90"></a>

虽然是英文界面，但是现在的浏览器都有网页翻译功能，鼠标点击右键，选择网页翻译即可翻译成中文。

注册并邮件激活账号，充值后即可购买服务器。充值方式是支付宝或paypal，使用paypal有银行卡（包括信用卡）即可。paypal注册地址：https://www.paypal.com （paypal是国际知名的第三方支付服务商，注册一下账号，绑定银行卡即可购买国外商品）

***

2.5美元/月的服务器配置信息：单核   512M内存  10G SSD硬盘   带宽1G    500G流量/月   (**不推荐，仅提供ipv6 ip，不推荐**)

3.5美元/月的服务器配置信息：单核   512M内存  10G SSD硬盘   带宽1G    500G流量/月   (**推荐**)

5美元/月的服务器配置信息：  单核   1G内存    25G SSD硬盘   带宽1G    1000G流量/月  (**推荐**)
 
10美元/月的服务器配置信息： 单核   2G内存    55G SSD硬盘   带宽1G    2000G流量/月  

20美元/月的服务器配置信息： 2cpu   4G内存   80G SSD硬盘    带宽1G    3000G流量/月  

40美元/月的服务器配置信息： 4cpu   8G内存   160G SSD硬盘   带宽1G    4000G流量/月  
 

***

**注意：2.5美元套餐只提供ipv6 ip，一般的电脑用不了，所以建议选择3.5美元及以上的套餐。**

vultr实际上是折算成小时来计费的，比如服务器是5美元1个月，那么每小时收费为5/30/24=0.0069美元 会自动从账号中扣费，只要保证账号有钱即可。如果你部署的服务器实测后速度不理想，你可以把它删掉（destroy），重新换个地区的服务器来部署，方便且实用。因为新的服务器就是新的ip，所以当ip被墙时这个方法很有用。当ip被墙时，为了保证新开的服务器ip和原先的ip不一样，先开新服务器，开好后再删除旧服务器即可。在账号的Billing选项里可以看到账户余额。

**账号充值如图**：

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/pp100.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/pp101.png)

**开通服务器步骤如图**：

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/vultr1.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/vultr2.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/vultr3.PNG)

### v2ray一键搭建脚本支持的系统有：Ubuntu 16+ / Debian 8+ / CentOS 7+ 系统

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/vultr-v2ray1.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/vultr5.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/vultr6.PNG)


**开通服务器时，当出现了ip，不要立马去ping或者用xshell去连接，再等5分钟之后，有个缓冲时间。完成购买后，找到系统的密码记下来，部署服务器时需要用到。vps系统的密码获取方法如下图：**

![](https://cdn.jsdelivr.net/gh/Alvin9999/crp_up/pac教程05.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/ss/Debian2.png)


**删掉服务器步骤如下图**：

删除服务器时，先开新的服务器后再删除旧服务器，这样可以保证新服务器的ip与旧ip不同。

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/ss/de4.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/ss/de2.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/ss/de5.png)

***

**第二步：部署VPS服务器**

购买服务器后，需要部署一下。因为你买的是虚拟东西，而且又远在国外，我们需要一个叫Xshell的软件来远程部署。Xshell windows版下载地址：

[国外云盘1下载](http://45.88.43.37/Xshell_setup_wm.exe)
[国外云盘2下载](http://tr1.freedown7.club/html/smallsoftware/Xshell_setup_wm.exe)  

如果你是Mac苹果电脑操作系统，更简单，无需下载xshell，系统可以直接连接VPS。直接打开Terminal终端，输入：ssh root@43.45.43.21（将45.45.43.21换成你的IP），之后输入你的密码就可以登录了（输入密码的时候屏幕上不会有显示）

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/Mac.png)

如果不能用Mac自带的终端连接的话，直接网上搜“Mac连接SSH的软件”，有很多，然后通过软件来连接vps服务器就行，具体操作方式参考windows xshell。Mac成功连接vps后剩下的操作和windows一样。

***

部署教程：

下载windows xshell软件并安装后，打开软件

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/xshell11.png)

选择文件，新建

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/xshell12.png)

随便取个名字，然后把你的服务器ip填上

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/xshell13.png)

连接国外ip即服务器时，软件会先后提醒你输入用户名和密码，用户名默认都是root，密码是你购买的服务器系统的密码。

**如果xshell连不上服务器，没有弹出让你输入用户名和密码的输入框，表明你开到的ip是一个被墙的ip，遇到这种情况，重新开新的服务器，直到能用xshell连上为止，耐心点哦！如果同一个地区开了多台服务器还是不行的话，可以换其它地区。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/xshell14.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/ss/xshell2.png)

连接成功后，会出现如上图所示，之后就可以复制粘贴代码部署了。

**Ubuntu 16+ / Debian 8+ / CentOS 7+ 系统 v2ray一键部署管理脚本**：

安装命令：

source <(curl -sL https://multi.netlify.app/v2ray.sh) --zh

升级命令(保留配置文件更新)：

source <(curl -sL https://multi.netlify.app/v2ray.sh) -k

卸载命令：

source <(curl -sL https://multi.netlify.app/v2ray.sh) --remove

> 安装完成后，输入v2ray可进入管理页面。脚本来自[Jrohy/multi-v2ray](https://github.com/Jrohy/multi-v2ray)。

> 脚本功能介绍：

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/v2ray/v2ray-fun1.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/v2ray/v2ray-fun2.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/v2ray/v2ray-fun3.PNG)

***

**脚本演示**

复制上面安装命令代码到VPS服务器里，复制代码用鼠标右键的复制，然后在vps里面右键粘贴进去，因为ctrl+c和ctrl+v无效。接着输入数字1来安装。安装完成后，如果想修改、查看配置等，可以输入v2ray进行管理页面，不用重复安装脚本。

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/v2ray/v2ray-2-1.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/v2ray/v2ray-2-2.PNG)

安装速度很快，安装结束后默认有个kcp协议帐号，如果不想用kcp协议，可以输入v2ray管理页面来进行传输方式的更改。

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/v2ray/v2ray-2-3.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/v2ray/v2ray-2-4.PNG)

**如果选择的是CentOS系统，还需要关闭vps防火墙来开放端口，相关命令如下：**

**查看防火墙状态命令：firewall-cmd --state**

**停止firewall命令：systemctl stop firewalld.service**

**禁止firewall开机启动命令：systemctl disable firewalld.service**


提醒：在教程的最后“常见问题参考解决方法”里面增加了高阶篇“一键部署WebSocket+Tls+Nginx+Web”的脚本,高级篇需要域名。

***


**第三步：一键加速VPS服务器**

五合一的TCP网络加速脚本，包括了BBR原版、BBR魔改版、暴力BBR魔改版、BBR plus、Lotsever(锐速)安装脚本。可用于KVMXen架构，不兼容OpenVZ（OVZ）。支持Centos 6+ / Debian 7+ / Ubuntu 14+，BBR魔改版不支持Debian 8。

***

wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh"

chmod +x tcp.sh

./tcp.sh


***

> 如果提示 wget: command not found 的错误，这是你的系统精简的太干净了，wget都没有安装，所以需要安装wget。CentOS系统安装wget命令: yum install -y wget Debian/Ubuntu系统安装wget命令:apt-get install -y wget

安装完成后，脚本管理命令为：./tcp.sh

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/newbbr1.jpg)

操作方法：先安装内核，重启vps让内核生效，再启动对应的加速即可。数字1的BBR/BBR魔改内核对应数字4、5、6的BBR加速、BBR魔改加速和暴力BBR魔改版加速。数字2的BBRplus内核对应数字7的BBRplus加速。数字3的锐速加速内核对应数字8的锐速加速。

以安装暴力BBR魔改版加速为例，我们先安装对应的内核，输入数字1

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/newbbr2.jpg)

内核安装完成后，输入y进行重启，重启才能让内核生效

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/newbbr3.jpg)

重启完成后，输入数字6来启动暴力BBR魔改版加速

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/newbbr4.jpg)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/newbbr5.jpg)

输入./tcp.sh查看最终是否启动成功。

如果想换一个加速，输入数字9进行卸载加速，然后进行同样的操作，安装内核再安装对应内核的加速即可。

**注意：如果在安装内核环节出现这样一张图，注意选择NO**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/newbbr6.jpg)

***

【v2ray客户端下载及使用方法】

**客户端使用教程：[v2ray各平台图文使用教程](https://github.com/Alvin9999/new-pac/wiki/v2ray%E5%90%84%E5%B9%B3%E5%8F%B0%E5%9B%BE%E6%96%87%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)**

浏览器代理设置成Socks(5) 127.0.0.1 和1080 即可通过v2ray代理上网。

谷歌浏览器chrome可配合switchyomega插件来使用，下载插件：[switchyomega](https://github.com/atrandys/trojan/releases/download/1.0.0/SwitchyOmega_Chromium.crx)

安装插件，打开chrome，打开扩展程序，将下载的插件拖动到扩展程序页面，添加到扩展。
![20181116000534](https://user-images.githubusercontent.com/12132898/70548725-0461d000-1bae-11ea-9d1e-4577e36ac46e.png)

完成添加，会跳转到switchyomega页面，点跳过教程，然后点击proxy，如图填写，最后点击应用选项。
![20181116001438](https://user-images.githubusercontent.com/12132898/70548727-04fa6680-1bae-11ea-99da-568af4fd6f5f.png)


***

**常见问题参考解决方法**：

1、账号无法使用，可能原因：vps防火墙端口没有放开或者本地电脑防火墙、杀毒软件阻挡代理软件。

关闭vps防火墙即可开放所有端口，本地电脑防火墙和杀毒软件手动关闭即可。

查看防火墙状态命令：firewall-cmd --state  

停止firewall命令：systemctl stop firewalld.service

禁止firewall开机启动命令：systemctl disable firewalld.service


2、搭建的账号之前能用，突然不能用了，怎么解决？

如果ip不能ping通，xshell不能直接连接vps服务器，说明ip被墙了，需要开新服务器换ip。

如果ip能ping，xshell能直接连接vps服务器，说明ip没有被墙，多半是端口被封了，优先换端口。

3、高阶篇

当封锁特别厉害的时候，常规的v2ray配置可能已经无法满足需求，这个时候我们可以尝试下WebSocket+Tls+Nginx+Web的方式，甚至搭建好后还可以套CDN，套CDN不是一个必须的步骤，但套CDN可以有效保护IP，甚至被墙的ip也能复活。套CDN的方法可以自行网络搜索。提前准备好域名，将域名指定vps的ip，然后根据脚本来搭建就好了。

有免费的域名，但为了稳定，建议选择付费的域名，因为免费的域名很可能会用不了多长时间。推荐用国外的域名服务商：[Namecheap](https://www.namecheap.com)，xyz、club后缀的域名1年1美元左右。


**一键部署WebSocket+Tls+Nginx+Web，支持系统Debian 8+ / Ubuntu 16.04+ / Centos7**：

***

wget -N --no-check-certificate -q -O install.sh "https://raw.githubusercontent.com/wulabing/V2Ray_ws-tls_bash_onekey/master/install.sh" && chmod +x install.sh && bash install.sh

***

![v2ray](https://user-images.githubusercontent.com/12132898/74119025-c22e2c80-4bf8-11ea-81fe-614133dcc713.PNG)

注意：ws+tls和http/2只能安装1个，不能同时安装。比如ws+tls安装后不好用，那么你可以卸载后安装http/2。

启动 V2ray：systemctl start v2ray

启动 Nginx：systemctl start nginx

安装完成后会得到v2ray账号信息，然后把账号信息填写到客户端里面，推荐用v2rayN客户端，参考[v2ray各平台图文使用教程
](https://github.com/Alvin9999/new-pac/wiki/v2ray%E5%90%84%E5%B9%B3%E5%8F%B0%E5%9B%BE%E6%96%87%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)

浏览器代理设置成Socks(5) 127.0.0.1 和1080

***

有问题可以发邮件至海外邮箱kebi2014@gmail.com