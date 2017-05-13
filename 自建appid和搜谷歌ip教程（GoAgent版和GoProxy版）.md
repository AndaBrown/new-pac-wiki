### 本教程用于GoAgent版和GoProxy版，这两款版本用的是相同的4000个appid，每个appid每天有1G流量，随着使用人数的增加，未来可能会满足不了，故出此教程。（每天北京时间下午4点谷歌流量会重置，也就是4点之后流量又是全新的）

### 此教程必须用GoProxy版来部署appid，所以从教程一开始，最好先启动GoProxy版，确保能正常翻墙上网。如果第一次启动GoProxy无法翻墙，请多启动几次。

**首先打开** https://console.cloud.google.com/appengine 

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid1.png)

PS：如果想注册google账号但没有手机号，一是可以用这个网站 https://www.textnow.com/ ，可以注册一个账号，然后该网站会分配给你一个美国号码，通常输入一下美国某个州的区号，然后就会给你一个那个州的号码；或者去淘宝上买个账号，或者代注册服务。淘宝有很多代收验证码的。

**按图操作后，创建自己的appid名字**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid2.png)

**稍等一会**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid3.png)

**在“您的第一个应用”下方选择“Python”**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid.png)

**为你的appid选择位置，有多个可以选择，如果不知道怎么选择，就选亚洲或美国**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid4.png)

**然后会开始创建**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid5.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid6.png)

**可以按照上述步骤，多创建几个appid，一个谷歌账号可以创建12个appid**

### 创建完毕后，开始进行部署流程

**打开**https://github.com/phuslu/goproxy-ci/releases/latest **下载** goproxy-gae-rXX.zip 服务端部署文件。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid7.png)

**下载后解压出来，然后打开gae文件夹里面的gae.go,必须用Notepad++打开，Notepad++下载地址**：http://rj.baidu.com/soft/detail/13478.html?ald  **下载后安装**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid8.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid9.png)

**下图指示的位置，可以为你的appid设置自己的密码，设置后记得保存 （此步骤可省略）**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid10.png)

**然后运行uploader.bat**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid11.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid12.png)

**在上图所示位置填上自己的appid名字，如果是多个appid，请用|分开 ，回车确定后，会弹出一个网址，请用翻墙软件打开，然后点击“允许”**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid13.png)

**之后开始自动部署**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid14.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid15.png)

**如果卡在某个步骤或者没有出现部署成功标志，关闭部署窗口，重新运行uploader.bat  **

**部署成功后，就可以用自己的appid替换软件自带的appid了。**

### 替换GoProxy版appid方法如下：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid16.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid17.png)

**打开Agent文件夹里面的gae.user.json,记得用Notepad++打开gae.user.json，然后如图：**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid18.png)

**输入自己的appid和密码即可，appid如果是多个的话，请按照原先的appid格式来弄**

### 替换GoAgent版appid方法如下：

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid19.png)

**打开Agent文件夹，然后用Notepad++打开proxy.user.ini**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/appid20.png)

**在上图所示位置填上自己的appid即可，如果是多个appid，请按照原先的appid格式来弄**

保存后就可以测试翻墙了，记得如果你填上自己的appid后，但之后你又运行ip更新文件，那么会覆盖你自己的appid，这个时候你需要自己再填一遍

**以上就是申请appid和部署appid的全部教程。等空了再写如何自己搜谷歌ip的教程。**


