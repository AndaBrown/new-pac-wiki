**介绍**:

ProxySU是一款windows科学上网搭建软件，支持一键搭建V2ray，Trojan，NaiveProxy, Trojan-Go, ShadowsocksR(SSR),Shadowsocks-libev及相关插件一键安装工具。

**使用提醒**：

ProxySU的安装流程，是假设在全新系统下，没有装过以上代理软件，如果已经安装过，最好将系统重装一下，会减少很多的麻烦。ProxySU在开发过程中，一般都是在[vultr](https://www.vultr.com/?ref=7048874)的vps中测试，测试系统版本为：Centos7/8 Debian9/10 Ubuntu18.04/20.04。[ProxySU官网](https://github.com/proxysu/windows/tree/v2.2.2)。

**ProxySU-v2.2.2功能如下:**

##### V2ray可一键安装的模式有：
* tcp 
* tcp+http伪装  
* tcp+TLS 
* tcp+TLS （自签证书）
* Vless+tcp+TLS+Web (新热门协议)
* WebSocket
* WebSocket+TLS 
* WebSocket+TLS+Web 
* WebSocket+TLS（自签证书） 
* http2  
* http2+TLS+Web
* http2（自签证书）
* mKCP及各种伪装 
* QUIC及各种伪装。  
注：mKCP和QUIC模式使用udp协议，可以有效减少网络延时，有加速的作用，但在网络管控严厉时期，会导致IP被封，遇到的一次，就是刚安装好，使用了3个小时后，IP被封（现已确认是mKCP的流量被识别导致，项目组正在维护中。2020.6.10维护完毕，升级到版本4.24.2及以上，启用mKCP密钥可增强抗识别）。以上模式最推荐的是WebSocket+TLS+Web 和http2+TLS+Web 需要有一个域名。如果能加上CDN则稳定性更好。加上CDN后，是加速还是减速，与线路有关。

##### Trojan 可一键安装：  
* Trojan + TLS + Web

##### Trojan-Go 可一键安装：  
* Trojan-Go + TLS + Web  
* Trojan-Go + WebSocket + TLS + Web

##### NaiveProxy一键安装：  
* NaiveProxy + TLS +Web  

##### ShadowsocksR(SSR)一键安装：  
* SSR+TLS+Caddy  

##### Shadowsocks-libev及相关插件一键安装：  
* SS 经典模式  
* SS+WebSocket+TLS+Caddy(Web前置) (推荐)  
* SS+WebSocket  
* SS+QUIC  
* SS+kcptun  
* SS+obfs+http+Web  
* SS+obfs+TLS+Web  

##### 支持的VPS系统为：  
* CentOS 7/8   
* Debian 8/9/10 (推荐 9)  
* Ubuntu 16.04及以上

示意图:

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps1.jpg)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps11.jpg)

**搭建流程**:

第一步:购买服务器获得ip和密码

第二步:ProxySU下载及搭建


***

**第一步:购买服务器获得ip和密码**

VPS服务器需要选择国外的，首选国际知名的vultr，速度不错、稳定且性价比高，按小时计费，能够随时开通和删除服务器，新服务器即是新ip。

vultr注册地址：https://www.vultr.com/?ref=7048874 （vps最低2.5美元/月，vultr全球17个服务器位置可选。支持支付宝和paypal付款。） 

<a href="https://www.vultr.com/?ref=7048874"><img src="https://www.vultr.com/media/banners/banner_728x90.png" width="728" height="90"></a>

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

**vps服务器推荐用Debain9，不推荐用CentOS7，CentOS7用ProxySU无法自动开启bbr加速。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/vultr4.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/vultr5.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/vultr/vultr6.PNG)


**开通服务器时，当出现了ip，不要立马去ping或者用ProxySU去连接，再等5分钟之后，有个缓冲时间。完成购买后，找到系统的密码记下来，部署服务器时需要用到。vps系统密码获取方法如下图：**

![](https://cdn.jsdelivr.net/gh/Alvin9999/crp_up/pac教程05.png)

![](https://cdn.jsdelivr.net/gh/Alvin9999/crp_up/pac教程06.png)

**删掉服务器步骤如下图**：

删除服务器时，先开新的服务器后再删除旧服务器，这样可以保证新服务器的ip与旧ip不同。

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/ss/de4.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/ss/de2.PNG)

![](https://cdn.jsdelivr.net/gh/Alvin9999/PAC/ss/de5.png)

**第二步:ProxySU下载及搭建**

**ProxySU**:[github官方下载](https://github.com/proxysu/windows/releases/tag/v2.2.2) **下载那个zip文件,下载后解压.**

如果github国内下载慢,可以用下面的网盘来下载. 

当前版本为ProxySU-v2.2.2,文件很小,大小为534kb.如果官方更新后,网盘会手动更新,如果没能及时更新,可以发邮件提醒我.

[国外云盘1下载](http://45.88.43.37/ProxySU-v2.2.2.zip) 
[国外云盘2下载](http://89.163.224.142/ProxySU-v2.2.2.zip) 
[国外云盘3下载](http://45.147.201.142/ProxySU-v2.2.2.zip) 

## Windows系统需要安装net4.0及以上

[Microsoft.NET Framework 4.0](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net40-offline-installer) or higher

打开ProxySU,填上第一步购买的vps服务器ip和密码后,选上想搭建的科学上网工具。步骤如下：

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps1.jpg)

**填上ip和密码，端口22和root默认。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps10.jpg)

**以搭建v2ray为例，选中v2ray模板库。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps3.jpg)

**在v2ray模板库中，选中想要搭建的v2ray协议，有的协议不需要域名，可以直接搭建，有的需要域名，所以需要提前购买域名并绑定服务器ip。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps4.jpg)

**目前比较热门的v2ray协议:WebSocket+Tls+Web （需要域名）选中后，填写域名。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps5.jpg)

**如果没有域名，可以搭建其它的协议，比如TCP、KCP。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps9.jpg)

**点击v2ray一键安装，软件会自动搭建。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps6.jpg)

**系统工具：点击系统工具可以校对时间和部署bbr加速。v2ray需要校对时间。目前搭建v2ray的过程中，软件自动校对时间和开启bbr加速，如果一切顺利不会手动再去点击系统工具。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps11.jpg)

**部署完后，会自动弹出帐号配置信息，并且在文件夹中也会自动生成相关配置文件及客户端下载地址。**

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps7.jpg)

![](https://cdn.jsdelivr.net/gh/Alvin9999/pac2/softimag/ps8.jpg)

还是比较人性化的。

***

###### V2ray模式目前已支持生成用于

* [v2ray官方程序](https://www.v2ray.com/chapter_00/install.html)配置文件(客户端配置)  
* [v2rayN (windows)](https://github.com/2dust/v2rayN/releases)客户端导入二维码和网址  
* [Qv2ray (windows)](https://github.com/Qv2ray/Qv2ray)客户端导入二维码和网址  
* [Shadowrocket (ios)](https://apps.apple.com/us/app/shadowrocket/id932747118)导入二维码和网址  
* [v2rayNG (Android)](https://github.com/2dust/v2rayNG/releases)导入二维码和网址  

（程序中只实现生成v2rayN的，但是Shadowrocket和v2rayNG都可以导入。）

###### Trojan模式目前已支持生成用于  

* [Trojan官方程序](https://github.com/trojan-gfw/trojan)配置文件（客户端配置）  
* [Trojan-QT5 (windows)](https://github.com/TheWanderingCoel/Trojan-Qt5/releases)导入二维码和网址  
* [Qv2ray (windows)](https://github.com/Qv2ray/Qv2ray)客户端导入二维码和网址  
* [Shadowrocket (ios)](https://apps.apple.com/us/app/shadowrocket/id932747118)导入二维码和网址  
* [igniter（Android）](https://github.com/trojan-gfw/igniter/releases)导入二维码和网址  
注：Trojan官方的Windows客户端，需要安装 [vc_redist.x64.exe](https://aka.ms/vs/16/release/vc_redist.x64.exe)。[官方说明](https://github.com/trojan-gfw/trojan/wiki/Binary-&-Package-Distributions#windows-vista)  

###### Trojan-Go模式目前已支持生成用于  

* [Trojan-Go官方程序](https://github.com/p4gefau1t/trojan-go/releases)配置文件（客户端配置）  
* [Trojan-QT5 (windows)](https://github.com/TheWanderingCoel/Trojan-Qt5/releases)导入二维码和网址(暂不支持WebSocket模式)  
* [Qv2ray (windows)](https://github.com/Qv2ray/Qv2ray)客户端导入二维码和网址  
* [Shadowrocket (ios)](https://apps.apple.com/us/app/shadowrocket/id932747118)导入二维码和网址(暂不支持WebSocket模式)  
* [igniter-go（Android）](https://github.com/p4gefau1t/trojan-go-android/releases)导入二维码和网址  

###### NaiveProxy支持生成用于：

* [NaiveProxy官方客户端](https://github.com/klzgrad/naiveproxy/releases)配置文件（windows客户端配置）  
* [NaiveGUI](https://github.com/ExcitedCodes/NaiveGUI/releases)(第三方Windows图形客户端)URL导入链接。  
* [Qv2ray (windows)](https://github.com/Qv2ray/Qv2ray)客户端导入二维码和URL  
注：这里多说几句NaiveProxy，现在墙越来越高，翻墙软件需要隐藏访问目标网址和加密数据的同时，还要隐藏自己的流量特征，不被识别出是代理流量。V2ray，Trojan都有其自己的实现。而NaiveProxy是配合Caddy的一个http.forwardproxy插件，插件有防嗅探，转发流量的功能。代理http流量很完美，但是在代理https流量时，会出现长度特征，NaiverProxy则弥补了这一点，消除了代理https时的流量特征，另外还应用 [Chrome's network stack](https://www.chromium.org/developers/design-documents/network-stack).更好的消除TLS的指纹特征。详细介绍请看项目官方介绍：[NaiveProxy官方文档](https://github.com/klzgrad/naiveproxy)。有兴趣的不妨一试。

###### SSR+TLS+Caddy 模式目前已支持生成用于  

* [ShadowsocksR (windows)](https://github.com/shadowsocksrr/shadowsocksr-csharp/releases)客户端导入二维码和URL  
* [SSRR（Android）](https://github.com/shadowsocksrr/shadowsocksr-android/releases)导入二维码和URL  
* [Shadowrocket (ios)](https://apps.apple.com/us/app/shadowrocket/id932747118)导入二维码和URL  

###### Shadowsocks-libev 目前已支持生成用于  

* [Shadowsocks (windows)](https://github.com/shadowsocks/shadowsocks-windows/releases)客户端导入二维码和URL  
* [shadowsocks（Android）](https://github.com/shadowsocks/shadowsocks-android/releases)导入二维码和URL  
* [Shadowrocket (ios)](https://apps.apple.com/us/app/shadowrocket/id932747118)导入二维码和URL  

***

有问题可以发邮件至海外邮箱kebi2014@gmail.com