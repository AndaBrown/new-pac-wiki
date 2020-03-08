**2020年2月12日更新。**

**本教程的图片被屏蔽了，可以访问https://blog.free-air.org/自建v2ray服务器教程**

***

**自建v2ray教程很简单，整个教程分三步**：

第一步：购买VPS服务器 

第二步：一键部署VPS服务器

第三步：一键加速VPS服务器 

***

**【前言】**

**v2ray的优势**：v2ray支持的传输方式有很多，包括：普通TCP、HTTP伪装、WebSocket流量、普通mKCP、mKCP伪装FaceTime通话、mKCP伪装BT下载流量、mKCP伪装微信视频流量，不同的传输方式其效果会不同，有可能会遇到意想不到的效果哦！当然国内不同的地区、不同的网络环境，效果也会不同，所以具体可以自己进行测试。现在v2ray客户端也很多了，有windows、MAC、linux和安卓版。

注意：如果你选择使用 V2ray，建议关闭并删除所有的ss/ssr服务端，避开互相干扰。

***

**第一步：购买VPS服务器**

VPS服务器需要选择国外的，首选国际知名的vultr，速度不错、稳定且性价比高，按小时计费，能够随时开通和删除服务器，新服务器即是新ip。

vultr注册地址：https://www.vultr.com/?ref=7048874  （最低2.5美元/月，全球15个服务器位置可选，KVM框架，最低2.5美元/月。）如果以后这个vultr注册地址被墙了，那么就用翻墙软件打开，或者用[ss/ssr免费账号](https://github.com/Alvin9999/new-pac/wiki/ss%E5%85%8D%E8%B4%B9%E8%B4%A6%E5%8F%B7)

<a href="https://www.vultr.com/?ref=7048874"><img src="https://www.vultr.com/media/banner_2.png" width="468" height="60"></a>

虽然是英文界面，但是现在的浏览器都有网页翻译功能，鼠标点击右键，选择网页翻译即可翻译成中文。

注册并邮件激活账号，充值后即可购买服务器。充值方式是支付宝或paypal，使用paypal有银行卡（包括信用卡）即可。paypal注册地址：https://www.paypal.com （paypal是国际知名的第三方支付服务商，注册一下账号，绑定银行卡即可购买国外商品）

***

2.5美元/月的服务器配置信息：单核   512M内存  10G SSD硬盘   带宽1G共享    500G流量/月   (**不推荐，仅提供ipv6 ip，不推荐**)

3.5美元/月的服务器配置信息：单核   512M内存  10G SSD硬盘   带宽1G共享    500G流量/月   (**推荐**)

5美元/月的服务器配置信息：  单核   1G内存    25G SSD硬盘   带宽1G共享    1000G流量/月  (**推荐**)
 
10美元/月的服务器配置信息： 单核   2G内存    55G SSD硬盘   带宽1G共享    2000G流量/月  

20美元/月的服务器配置信息： 2cpu   4G内存   80G SSD硬盘    带宽1G共享    3000G流量/月  

40美元/月的服务器配置信息： 4cpu   8G内存   160G SSD硬盘   带宽1G共享    4000G流量/月  
 

***

**注意：2.5美元套餐只提供ipv6 ip，一般的电脑用不了，所以建议选择3.5美元及以上的套餐。**

vultr实际上是折算成小时来计费的，比如服务器是5美元1个月，那么每小时收费为5/30/24=0.0069美元 会自动从账号中扣费，只要保证账号有钱即可。如果你部署的服务器实测后速度不理想，你可以把它删掉（destroy），重新换个地区的服务器来部署，方便且实用。因为新的服务器就是新的ip，所以当ip被墙时这个方法很有用。当ip被墙时，为了保证新开的服务器ip和原先的ip不一样，先开新服务器，开好后再删除旧服务器即可。在账号的Billing选项里可以看到账户余额。

**账号充值如图**：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/pp100.png)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/pp101.png)

**开通服务器步骤如图**：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/vultr/vultr1.PNG)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/vultr/vultr2.PNG)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/vultr/vultr3.PNG)

### v2ray一键搭建脚本支持的系统有：Debian 8、Debian 7、Ubuntu 14、Ubuntu 16、CentOS 7。（注意：不支持CentOS 6和8系统！）

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/vultr/vultr-v2ray1.png)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/vultr/vultr5.PNG)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/vultr/vultr6.PNG)



**开通服务器时，当出现了ip，不要立马去ping或者用xshell去连接，再等5分钟之后，有个缓冲时间。完成购买后，找到系统的密码记下来，部署服务器时需要用到。vps系统的密码获取方法如下图：**

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程05.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian2.png)


**删掉服务器步骤如下图**：

删除服务器时，先开新的服务器后再删除旧服务器，这样可以保证新服务器的ip与旧ip不同。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/de4.PNG)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/de2.PNG)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/de5.png)

一个被墙ip的vps被删掉后，其ip并不会消失，会随机分配给下一个在这个服务器位置新建服务器的人，这就是为什么开新服务器会有一定几率开到被墙的ip。被墙是指在国内地区无法ping通服务器，但在国外是可以ping通的，vultr是面向全球服务，如果这个被墙ip被国外的人开到了，它是可以被正常使用的，一般一段时间后就会被解封，那么这就是一个良性循环。

***

**第二步：部署VPS服务器**

购买服务器后，需要部署一下。因为你买的是虚拟东西，而且又远在国外，我们需要一个叫Xshell的软件来远程部署。Xshell windows版下载地址：

[国外云盘下载](http://www.freedown9.com/html/smallsoftware/Xshell_setup_wm.exe) 
[国外云盘2下载](http://108.61.224.82/lib5/Xshell_setup_wm.exe)

如果你是Mac苹果电脑操作系统，更简单，无需下载xshell，系统可以直接连接VPS。直接打开Terminal终端，输入：ssh root@43.45.43.21（将45.45.43.21换成你的IP），之后输入你的密码就可以登录了（输入密码的时候屏幕上不会有显示）

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/Mac.png)

如果不能用Mac自带的终端连接的话，直接网上搜“Mac连接SSH的软件”，有很多，然后通过软件来连接vps服务器就行，具体操作方式参考windows xshell。Mac成功连接vps后剩下的操作和windows一样。

***

部署教程：

下载windows xshell软件并安装后，打开软件

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell11.png)

选择文件，新建

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell12.png)

随便取个名字，然后把你的服务器ip填上

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell13.png)

连接国外ip即服务器时，软件会先后提醒你输入用户名和密码，用户名默认都是root，密码是你购买的服务器系统的密码。

**如果xshell连不上服务器，没有弹出让你输入用户名和密码的输入框，表明你开到的ip是一个被墙的ip，遇到这种情况，重新开新的服务器，直到能用xshell连上为止，耐心点哦！如果同一个地区开了多台服务器还是不行的话，可以换其它地区。**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell14.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/xshell2.png)

连接成功后，会出现如上图所示，之后就可以复制粘贴代码部署了。

**Debian8/Debian7/Ubuntu16/Ubuntu14/CentOS7 v2ray一键部署管理脚本**：

安装脚本命令：

***

wget -N --no-check-certificate https://raw.githubusercontent.com/KiriKira/v2ray.fun/kiriMod/install.sh && bash install.sh


***

卸载脚本命令：


***

wget -N --no-check-certificate https://raw.githubusercontent.com/KiriKira/v2ray.fun/kiriMod/uninstall.sh && bash uninstall.sh


***

> 如果提示 wget: command not found 的错误，这是你的系统精简的太干净了，wget都没有安装，所以需要安装wget。CentOS系统安装wget命令: yum install -y wget  Debian/Ubuntu系统安装wget命令:apt-get install -y wget

———————————————————代码分割线————————————————

复制上面的代码到VPS服务器里，复制代码用鼠标右键的复制，然后在vps里面右键粘贴进去，因为ctrl+c和ctrl+v无效。接着按回车键，脚本会自动安装。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian4.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian5.png)

如上图，输入快捷管理命令v2ray后，开始进行v2ray服务端配置。以后只需要运行这个快捷命令就可以出现下图的界面进行设置，快捷管理命令为：v2ray

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian7.png)

如上图，输入数字2进行更改配置，共有6个子选项，包括：更改UUID、更改主端口、更改加密方式、更改传输方式、更改TLS设置（有域名才行）、更改广告拦截功能。（更改TLS设置和更改广告拦截功能不用设置）

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian8.png)

如上图，输入数字1来更改新的UUID号，弹出提示后，输入字母y来确认。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian9.png)

修改UUID号，界面会回到v2ray主界面，重新输入2进入更改配置选项，在输入数字2来更改主端口，主端口范围40～65535，理论上可以任意设置，但不要以0开头！

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian10.png)

重新进入更改配置选项，输入数字3来更改加密方式，加密方式有4种，最后1种为不加密。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian11.png)

**接着，进行传输方式的设置，传输方式共有7种，这个配置对v2ray的速度起着很大的作用，具体哪个最适合你那里的网络环境，需要你自己来尝试。**

**注意：普通TCP、普通mKCP、mKCP伪装FaceTime通话、mKCP伪装BT下载流量、mKCP伪装微信视频流量可直接设置、不需要域名，HTTP伪装和WebSocket流量需要你有域名，且域名绑定了你的vps服务器ip。(在教程的最后“常见问题参考解决方法”里面增加了专门部署ws+tls的脚本)**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian12.png)

进行了更改配置的设置后，输入数字3可以查看自己设置的v2ray信息。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian13.png)

**最后一步很关键，那就是启动服务，进入主界面后，输入数字1，然后输入1启动v2ray服务。以后，每次你更改配置或重启vps服务器后都要进行启动服务，请牢记！**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian14.png)

采用xshell软件，可以很方便的将配置文件导出，方便配置windows v2ray客户端。选择数字4，出现提示后，输入字母y，选择电脑路径即可。

> 如果你没有用xshell软件，那么无法使用脚本的文件导出功能。vps服务器里面的config.json配置文件存放路径为 /etc/v2ray/config.json MAC电脑用户可以用WinSCP MAC版连接vps服务器，然后根据路径把config.json文件复制出来。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian15.png)

**下面这个config.json文件就是我们刚刚配置的v2ray文件，如果以后更改了v2ray服务端信息，那么你需要重新导出config.json文件。**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian16.png)

**因为一键搭建v2ray脚本是一个循环脚本，当你配置结束后不会自动退出快捷管理命令，如果你想退出界面进行其它操作，可以同时按下键盘上的ctrl键和字母z键。**

**注意：以上直接下载并替换config文件的方法只适合v2ray官方客户端，像第三方开发的客户端，比如v2rayN、v2rayX是不适合用直接替换config文件的方法。如果用第三方开发的客户端的话，可以按照要求填写账号信息，如果部署的账号信息没有额外ID，在第三方客户端的额外ID那一栏一般是可以随便填写一个数字，比如1～10选1个。参考教程：[v2ray各平台图文使用教程](https://github.com/Alvin9999/new-pac/wiki/v2ray%E5%90%84%E5%B9%B3%E5%8F%B0%E5%9B%BE%E6%96%87%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)**


***


**第三步：一键加速VPS服务器**

**总共有2种加速方法，bbr加速和锐速加速，选择1种。**

**【加速教程1：谷歌BBR加速教程】**


***

wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh

chmod +x bbr.sh

./bbr.sh


***

把上面整个代码复制后粘贴进去，不动的时候按回车，然后耐心等待。最后输入reboot来重启服务器，确保加速生效，bbr加速脚本是开机自动启动，装一次就可以了。

演示开始，如图：

复制并粘贴代码后，按回车键确认

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/18.png)

如下图提示，按任意键继续部署

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/19.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian19.png)

整个部署过程需要2～5分钟，最后输入reboot来重启服务器，确保加速生效，bbr加速脚本是开机自动启动，装一次就可以了。

服务器重启成功并重新连接服务器后，输入命令lsmod | grep bbr  如果出现tcp_bbr字样表示bbr已安装并启动成功。如图：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/demo/tcp_bbr.PNG)

**注意**：根据反馈，少部分人安装bbr脚本并重启后，几分钟过去了，发现xshell无法连接服务器且服务器ip无法ping通。解决方法是：开新服务器或者重装系统，然后先安装bbr脚本再安装v2ray脚本。或者换锐速加速。

重装系统方法，点击vultr服务器设置界面——“Server Reinstall”，如下图：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/demo/reinstall.png)

重装过程一般需要5～10分钟。

**【加速教程2：破解版锐速加速教程】**

**第一步，先更换服务器内核（脚本只支持centos系统，其它系统可以直接尝试第二步）**


***

yum -y install wget

wget --no-check-certificate https://blog.asuhu.com/sh/ruisu.sh && bash ruisu.sh


***

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/rs1.PNG)

不动的时候敲回车键，在上图时需要多等一会儿。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/rs2.PNG)

出现上图时表示已成功替换内核并服务器自动重启。

**完成后会重启，2分钟后重新连接服务器，连上后开始第二步的操作。**

**第二步，一键安装锐速**


***

wget -N --no-check-certificate https://raw.githubusercontent.com/91yun/serverspeeder/master/serverspeeder-all.sh && bash serverspeeder-all.sh


***

卸载加速代码命令为：


***

chattr -i /serverspeeder/etc/apx* && /serverspeeder/bin/serverSpeeder.sh uninstall -f


***

但有些内核是不适合的，部署过程中需要手动选择推荐的，当部署时出现以下字样：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/%E9%94%90%E9%80%9F2.PNG)

提示没有完全匹配的内核,随便选一个内核就行,按照提示来输入数字,按回车键即可

锐速安装成功标志如下：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/%E9%94%90%E9%80%9F3.png)

出现running字样即可!


***

**需要注意的是：不管是重启服务器，还是以后想修改之前vps里面的v2ray配置信息，当你重启好服务器或者修改好了v2ray配置信息后，都需要启动v2ray服务端。方式是：输入v2ray，选择1，然后选择1（启动服务）。**

***

【v2ray客户端下载】

**2019年12月11日更新。**

[v2ray各平台客户端下载地址](https://github.com/v2ray/v2ray-core/releases)

[v2ray iOS客户端下载地址](https://itunes.apple.com/cn/app/kitsunebi/id1275446921?mt=8)

[v2ray 安卓客户端下载地址](https://play.google.com/store/apps/details?id=com.github.dawndiy.bifrostv) [v2rayNG下载地址](https://github.com/2dust/v2rayNG/releases)

以v2ray windows版为例：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian17.png)

下载windows版客户端后解压出来，然后替换config.json配置文件。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian18.png)

运行上图中的v2ray.exe启动软件，浏览器代理设置成Socks(5) 127.0.0.1 和1080 即可通过v2ray代理上网。

谷歌浏览器chrome可配合switchyomega插件来使用，下载插件：[switchyomega](https://github.com/atrandys/trojan/releases/download/1.0.0/SwitchyOmega_Chromium.crx)

安装插件，打开chrome，打开扩展程序，将下载的插件拖动到扩展程序页面，添加到扩展。
![20181116000534](https://user-images.githubusercontent.com/12132898/70548725-0461d000-1bae-11ea-9d1e-4577e36ac46e.png)

完成添加，会跳转到switchyomega页面，点跳过教程，然后点击proxy，如图填写，最后点击应用选项。
![20181116001438](https://user-images.githubusercontent.com/12132898/70548727-04fa6680-1bae-11ea-99da-568af4fd6f5f.png)

**注意：以上直接下载并替换config文件的方法只适合v2ray官方客户端，像第三方开发的客户端，比如v2rayN、v2rayX是不适合用直接替换config文件的方法。如果用第三方开发的客户端的话，可以按照要求填写账号信息，额外ID可以随便填个，比如1～10。参考教程：[v2ray各平台图文使用教程](https://github.com/Alvin9999/new-pac/wiki/v2ray%E5%90%84%E5%B9%B3%E5%8F%B0%E5%9B%BE%E6%96%87%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)**

***

**常见问题参考解决方法**：

1、账号无法使用，可能原因一：**客户端与服务端的设备系统时间相差过大。**

当vps服务器与本地设备系统时间相差过大，会导致客户端无法与服务端建立链接。请修改服务器时区，再手动修改服务器系统时间（注意也要校准自己本地设备时间）！

先修改vps的时区为中国上海时区：\cp -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime 

再手动修改vps系统时间命令的格式为（数字改为和自己电脑时间一致，误差30秒以内）：date -s "2018-11-02 19:14:00"   

修改后再输入date命令检查下。

2、账号无法使用，可能原因二：**Windows 防火墙、杀毒软件阻挡代理软件。**

如果以上问题都已排查，可以关闭 Windows 自带的防火墙、杀毒软件再尝试。

3、搭建的账号之前能用，突然不能用了，怎么解决？

如果ip不能ping通，xshell不能直接连接vps服务器，说明ip被墙了，需要开新服务器换ip。

如果ip能ping，xshell能直接连接vps服务器，说明ip没有被墙，多半是端口被封了，优先换端口。

4、高阶篇

当封锁特别厉害的时候，常规的v2ray配置可能已经无法满足需求，这个时候我们可以尝试下ws+tls的方式，甚至搭建好后还可以套CDN，套CDN不是一个必须的步骤，但套CDN可以有效保护IP，甚至被墙的ip也能复活。套CDN的方法可以自行网络搜索。提前准备好域名，将域名指定vps的ip，然后根据脚本来搭建就好了。

有免费的域名，但为了稳定，建议选择付费的域名，因为免费的域名很可能会用不了多长时间。推荐用国外的域名服务商：[Namecheap](https://www.namecheap.com)，xyz、club后缀的域名1年1美元左右。


**一键部署Nginx+ws+tls脚本，支持系统Debian 8+ / Ubuntu 16.04+ / Centos7**：

***

bash <(curl -L -s https://raw.githubusercontent.com/wulabing/V2Ray_ws-tls_bash_onekey/master/install.sh) | tee v2ray_ins.log

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