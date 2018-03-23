**2018年3月23日发布,待完善。**

### 不怕被封ip，因为vultr是折算成小时计费，且可以随时删除和开通服务器，新服务器就是新的ip。新开服务器只需要0.01美元，即使你运气非常不好，开了10台服务器才获得没有被墙的ip，总创建服务器成本也只有0.1美元，不到1块钱。


**自建v2ray教程很简单，整个教程分三步**：

第一步：购买VPS服务器 

第二步：一键部署VPS服务器

第三步：一键加速VPS服务器 （谷歌BBR加速，推荐）

【前言】

**v2ray的优势**：v2ray支持的传输方式有很多，包括：普通TCP、HTTP伪装、WebSocket流量、普通mKCP、mKCP伪装FaceTime通话、mKCP伪装BT下载流量、mKCP伪装微信视频流量，不同的传输方式其效果会不同，有可能会遇到意想不到的效果哦！当然国内不同的地区、不同的网络环境，效果也会不同，所以具体可以自己进行测试。

**v2ray的劣势**：目前v2ray支持的客户端种类不多，官网是上只有windows、MAC和linux版，苹果版和安卓版客户端至少官网上没有。关于客户端种类，ss/ssr是比较成熟的，这是ss/ssr的优势，但ss/ssr也有劣势，就是因为使用人数有点多，有可能以后会被专门针对进行干扰，所以多学一种翻墙技能有好处。

**第一步：购买VPS服务器**

VPS服务器需要选择国外的，首选国际知名的vultr，速度不错、稳定且性价比高，按小时计费，能够随时开通和删除服务器，新服务器即是新ip。

vultr注册地址： http://www.vultr.com/?ref=7048874 （全球15个服务器位置可选，KVM框架，最低2.5美元/月。如果以后这个vultr注册地址被墙了，那么就用翻墙软件打开，或者用[ss/ssr免费账号](https://github.com/Alvin9999/new-pac/wiki/ss%E5%85%8D%E8%B4%B9%E8%B4%A6%E5%8F%B7)） 

<a href="https://www.vultr.com/?ref=7048874"><img src="https://www.vultr.com/media/banner_2.png" width="468" height="60"></a>

虽然是英文界面，但是现在的浏览器都有网页翻译功能，鼠标点击右键，选择网页翻译即可翻译成中文。

注册并邮件激活账号，充值后即可购买服务器。充值方式是paypal（首选）或支付宝，使用paypal有银行卡（包括信用卡）即可。paypal注册地址：https://www.paypal.com （paypal是国际知名的第三方支付服务商，注册一下账号，绑定银行卡即可购买国外商品）

2.5美元/月的服务器配置信息：单核   512M内存  20G SSD硬盘   带宽峰值100M    500G流量/月   

5美元/月的服务器配置信息：  单核   1G内存    25G SSD硬盘   带宽峰值100M    1000G流量/月  
 
10美元/月的服务器配置信息： 单核   2G内存    40G SSD硬盘   带宽峰值100M    2000G流量/月  

20美元/月的服务器配置信息： 2cpu   4G内存   60G SSD硬盘    带宽峰值100M    3000G流量/月  

40美元/月的服务器配置信息： 4cpu   8G内存   100G SSD硬盘   带宽峰值100M    4000G流量/月  

**vultr实际上是折算成小时来计费的，比如服务器是5美元1个月，那么每小时收费为5/30/24=0.0069美元 会自动从账号中扣费，只要保证账号有钱即可。如果你部署的服务器实测后速度不理想，你可以把它删掉（destroy），重新换个地区的服务器来部署，方便且实用。因为新的服务器就是新的ip，所以当ip被墙时这个方法很有用。当ip被墙时，为了保证新开的服务器ip和原先的ip不一样，先开新服务器，开好后再删除旧服务器即可。**


计费从你开通服务器开始算的，不管你有没有使用，即使服务器处于关机状态仍然会计费，如果你没有开通服务器就不算。比如你今天早上开通了服务器，但你有事情，晚上才部署，那么这段时间是会计费的。同理，如果你早上删掉服务器，第二天才开通新的服务器，那么这段时间是不会计费的。在账号的Billing选项里可以看到账户余额。

温馨提醒：同样的服务器位置，不同的宽带类型和地区所搭建的账号的翻墙速度会不同，这与中国电信、中国联通、中国移动国际出口带宽和线路不同有关，所以以实测为准。可以先选定一个服务器位置来按照教程进行搭建，熟悉搭建方法，当账号搭建完成并进行了bbr加速后，测试下速度自己是否满意，如果满意那就用这个服务器位置的服务器。如果速度不太满意，就一次性开几台不同的服务器位置的服务器，然后按照同样的方法来进行搭建并测试，选择最优的，之后把其它的服务器删掉，按小时计费测试成本可以忽略。

**账号充值如图**：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/pp100.png)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/pp101.png)


**开通服务器步骤如图**：

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程01.png)

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程02.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian1.png)


### 为了配合第三步的v2ray一键搭建脚本，vps操作系统推荐选择Debian 8，其它支持系统有Debian 7、Ubuntu 14、Ubuntu 16、CentOS 7。（注意：不支持centos 6系统！centos 6是ss/ssr搭建教程的推荐系统，但centos 6不支持v2ray一键搭建脚本！）

**完成购买后，找到系统的密码记下来，部署服务器时需要用到。vps系统（推荐Debian 8）的密码获取方法如下图：**

![](https://raw.githubusercontent.com/Alvin9999/crp_up/master/pac教程05.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian2.png)


**删掉服务器步骤如下图**：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/de4.PNG)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/de2.PNG)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/de5.png)


***

**第二步：部署VPS服务器**

购买服务器后，需要部署一下。因为你买的是虚拟东西，而且又远在国外，我们需要一个叫Xshell的软件来远程部署。Xshell windows版下载地址：

[国外云盘1下载](http://45.32.141.248:8000/f/d91974d046/) 

[国外云盘2下载](https://nofile.io/f/eb5dUzYMQK4/Xshell_setup_wm.exe) 提取密码：666

[国外云盘3下载](https://www.adrive.com/public/NdK3Ez/Xshell_setup_wm.exe) 密码：123

如果你是苹果电脑操作系统，更简单，无需下载xshell，系统可以直接连接VPS。打开**终端**（Terminal），输入ssh root@ip  其中“ip”替换成你VPS的ip, 按回车键，然后复制粘贴密码，按回车键即可登录。粘贴密码时有可能不显示密码，但不影响， [参考设置方法](http://www.cnblogs.com/ghj1976/archive/2013/04/19/3030159.html)  如果不能用MAC自带的终端连接的话，直接网上搜“MAC连接SSH的软件”，有很多，然后通过软件来连接vps服务器就行，具体操作方式参考windows xshell。

***

部署教程：

下载windows xshell软件并安装后，打开软件

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell11.png)

选择文件，新建

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell12.png)

随便取个名字，然后把你的服务器ip填上

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell13.png)

连接国外ip即服务器时，软件会先后提醒你输入用户名和密码，用户名默认都是root，密码是你购买的服务器系统的密码。

### 如果xshell连不上服务器，没有弹出让你输入用户名和密码的输入框，表明你开到的ip是一个被墙的ip，遇到这种情况，重新开新的服务器，直到能用xshell连上为止，耐心点哦！如果同一个地区开了多台服务器还是不行的话，可以换其它地区。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/xshell14.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/xshell2.png)

连接成功后，会出现如上图所示，之后就可以复制粘贴代码部署了。

Debian8（推荐）/Debian7/Ubuntu16/Ubuntu14/centos7 v2ray一键部署管理脚本：

安装脚本命令：

bash -c "$(curl -fsSL https://raw.githubusercontent.com/tracyone/v2ray.fun/master/install.sh)"

卸载脚本命令：

bash -c "$(curl -fsSL https://raw.githubusercontent.com/tracyone/v2ray.fun/master/uninstall.sh)"

———————————————————代码分割线————————————————

复制上面的代码到VPS服务器里，复制代码用鼠标右键的复制，然后在vps里面右键粘贴进去，因为ctrl+c和ctrl+v无效。接着按回车键，脚本会自动安装，以后只需要运行这个快捷命令就可以出现下图的界面进行设置，快捷管理命令为：v2ray


![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian3.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian4.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian5.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian7.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian8.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian9.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian10.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian11.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian12.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian13.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian14.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian15.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/ss/Debian16.png)