如果你排除了杀毒软件和防火墙的干扰，那么你可以通过手动设置DNS的方法来解决。例如：在PAC代理地址没有失效的前提下，上海电信使用PAC版无效，一个PAC地址都没法使用。（可以使用goagent、goproxy、蓝灯版）

DNS设置教程：

阿里 DNS 设置教程 http://www.alidns.com/setup/?spm=0.0.0.0.YS7xRC

百度 DNS 设置教程 http://dudns.baidu.com/support/faqs/

Windows XP/7/8/10 - Mac OS DNS 设置教程 https://support.dnspod.cn/Kb/showarticle/tsid/240/#link1  

或者在路由器中将 DNS 设为第三方 DNS，一劳永逸。百度 DNS 路由器设置教程：http://dudns.baidu.com/support/localdns/Router/


**DNS 服务器**

DNSPOD DNS （首选）       119.29.29.29

DNSPod Public DNS + 在深圳、上海、天津、香港和北美部署了接入集群，通过 BGP Anycast 技术，在国内与全国 Top 16 运营商（电信、联通、移动、教育网、长宽、天威、铁通、电信通、歌华有线、东方有线、杭州华数、方正宽带、广东盈通、中信网络、CNISP、陕西广电）进行了对等互联，并可以无缝扩展，无论用户处于何地都可以就近快速访问 DNSPod 的公共 DNS，最快得到解析结果，提升网络访问体验。
DNSPod 公共 DNS 服务端使用 DPDK 开发，万兆网络接入，高效的全缓存设计，确保对用户的解析请求作出快速的应答。

阿里 AliDNS              223.5.5.5

阿里公共 DNS 在多个骨干网节点机房部署 DNS 服务器集群，采用 BGP anycast 技术宣告统一服务 IP：223.5.5.5 和 223.6.6.6，接收并应答客户请求.

阿里公共 DNS 通过多机房高可用架构、自研的高性能 DNS 系统和优化的 DNS 缓存技术，能为用户提供更加稳定、无劫持广告的 DNS 递归解析服务。

114 DNS              114.114.114.114 

114DNS 由几百个 Intel 的高端 CPU 内核构成，有多条 10GE 和 GE 电路直连电信运营商的核心路由器，采用 BGP Global AnyCast 技术多点部署。截止到 2014 年 5 月，114DNS 的公众 DNS 服务将中国除港澳台之外的地区划分为 58 个逻辑片区，中国电信 19 个，中国联通 16 个，中国移动 20 个，铁通、教育科研网、美国各 1 个。


百度 DNS             180.76.76.76 

百度公共 DNS 采用 bgp anycast 技术对外提供服务，目前已经接入包括联通、电信、移动、教育网、长城宽带、方正宽带、铁通、华数、世纪互联、东方有线等在内的多个运营商，具有业界一流的网络覆盖以及速度和稳定性体验。

更多公共 DNS: http://dns.ip.cn/

公共 DNS 相对 本地 DNS主要优势在于解析速度快、防污染。部分 DNS 比如114.114.114.114可以加速苹果商店 appstore 的下载速度。

***

**全平台清除 DNS 缓存方法**

**Windows 点击左下角开始键，运行 cmd ,在命令提示符运行命令 ipconfig /flushdns**

OS X 10.9OS X 10.10.4+ 在［应用程序］［实用工具］［终端］运行命令 

sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder

OS X 10.10 在［应用程序］［实用工具］［终端］运行命令 sudo discoveryutil udnsflushcaches

OS X 10.7 ~ 10.8 在［应用程序］［实用工具］［终端］运行命令 sudo killall -HUP mDNSResponder

Linux 在［终端］运行命令 /etc/rc.d/init.d/nscd restart

Android、iOS 打开飞行模式 在关闭 重复3次，在重启设备
