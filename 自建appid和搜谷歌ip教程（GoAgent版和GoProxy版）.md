**2017年9月19日更新第二部分的搜ip教程。主要更新内容：更新google ip段在线地址库，新增搜ip软件MFF xp版。**

在线ip段地址：https://raw.githubusercontent.com/Alvin9999/PAC/master/google%20ip%20duan

打开上面的地址，把里面的ip段复制到文件夹中的的“内置ip段.txt"文件即可，本次ip段总ip数417万。

***

**本教程用于GoAgent版和GoProxy版，这两款版本用的是相同的4000个appid，每个appid每天有1G流量，随着使用人数的增加，未来可能会满足不了，故出此教程。（每天北京时间下午4点谷歌流量会重置，也就是4点之后流量又是全新的）虽然我会不定期对GoAgent版和GoProxy版进行更新ip，但出个教程还是可以给想学习的人一个机会。**

### 第一部分——自建APPID教程

**此教程必须用GoProxy版来部署appid，所以从教程一开始，最好先启动GoProxy版，确保能正常翻墙上网。如果第一次启动GoProxy无法翻墙，请多启动几次。**

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

**打开**https://github.com/phuslu/goproxy-ci/releases/tag/r1527 **下载** goproxy-gae-r73.zip 服务端部署文件。

[备用下载地址](https://www.babel.cc/share.do?s=5628706171695177)

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/r73.PNG)

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

**以上就是申请appid和部署appid的全部教程**


***

### 第二部分——自己搜谷歌ip教程

**首先电脑先安装NET4.6或NET4.0，XP系统装4.0的。如果不安装NET，没法正常运行搜ip工具。然后下载搜ip工具——MFF**

win7、win8、win10版 MFF_net4.6_v2017.9.19.rar [百度云盘下载](https://pan.baidu.com/s/1mi3Ml4W) 密码：73mg  （第一次打开如果出现页面不存在，刷新一下网页）

win xp版 MFF_net4.0_v2017.9.19.rar [百度云盘下载](https://pan.baidu.com/s/1gfIj8jT) 密码：is77 （第一次打开如果出现页面不存在，刷新一下网页）

**下载后解压出来；使用前要先退出杀毒软件，以免被误报，如果不幸被误删了，请重新解压**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/搜ip1.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/搜ip2.png)

运行搜ip工具（ps：该工具由网友开发分享，工具名字有点不雅，请见谅）

**把名字为“内置ip段.txt"文件拖到搜ip工具中，就可以自动导入“内置ip段.txt"里面的ip，或者点击软件界面上的“测试ip池”上面的下拉菜单，选择“内置ip段”也可以导入ip。**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/搜ip3.png)

**关于线程数和超时说明如图：**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/搜ip4.png)

**我把线程数调到了400，超时300，搜了几分钟后，搜到了44个ip**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/搜ip5.png)

### 单击延迟按钮可以将搜到的ip进行排序。特别提醒：每个ip都能看到归属地，如果发现有归属地为中国的，搜完ip后将它去除，因为归属地为中国的ip不仅仅没法使用，如果和国外的ip混在一起还会起干扰作用，会影响正常翻墙。

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/搜ip6.png)

**选中要导入的ip，右键，如果是要导入到GoProxy版，请选择第一个；如果是要导入到GoAgent版，请选择第三个**

**以GoAgent版为例，选择第三个ip格式后，打开GoAgent版的proxy.user.ini，替换前面两行，第三行为gws ip，把你之前搜到的ip按ip类型排序，然后选中gws ip复制到第三行即可**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/搜ip7.png)

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/搜ip8.png)

**以GoProxy版为例，选择第一个ip格式后，打开GoProxy版的gae.user.json，替换如图所示的那行即可，GoProxy版不分gws和gvs ip**

![](https://raw.githubusercontent.com/Alvin9999/PAC/master/搜ip9.png)

**替换ip之后点击保存，然后亲测翻墙。**

**自己搜ip一般2周搜一次即可，特殊情况除外。通常自己搜的ip会更加适应自己的网络环境。**

以上就是全部教程了，有问题可以发邮件到kebi2014@gmail.com