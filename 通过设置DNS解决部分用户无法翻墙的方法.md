如果你排除了杀毒软件和防火墙的干扰，那么你可以通过手动设置DNS的方法来尝试着解决。

DNS设置教程：

阿里 DNS 设置教程 http://www.alidns.com/setup/?spm=0.0.0.0.YS7xRC

百度 DNS 设置教程 http://dudns.baidu.com/support/faqs/

Windows XP/7/8/10 - Mac OS DNS 设置教程 https://support.dnspod.cn/Kb/showarticle/tsid/240/#link1  



**DNS 服务器**

DNSPOD DNS （首选）       119.29.29.29

阿里 AliDNS              223.5.5.5

114 DNS              114.114.114.114 

百度 DNS             180.76.76.76 


更多公共 DNS: http://dns.ip.cn/

公共 DNS 相对 本地 DNS主要优势在于解析速度快、防污染。部分 DNS 比如114.114.114.114可以加速苹果商店 appstore 的下载速度。

***

**全平台清除 DNS 缓存方法**

**Windows 点击左下角开始键，运行 cmd ,在命令提示符运行命令 ipconfig /flushdns**

Android、iOS 打开飞行模式 在关闭 重复3次，在重启设备

Linux 在【终端】运行命令 /etc/rc.d/init.d/nscd restart

OSX10.7 ~ 10.8 在【应用程序】-【实用工具】-【终端】运行命令 sudo killall -HUP mDNSResponder

OS X 10.9～OS X 10.10.4+ 在【应用程序】-【实用工具】-【终端】运行命令 sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder

OSX10.10 在【应用程序】-【实用工具】-【终端】运行命令 sudo discoveryutil udnsflushcaches



