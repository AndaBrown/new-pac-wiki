ubuntu 安装 shadowsocks，配合shadowsocks账号就能翻墙，[点我获取最新ss免费账号](https://github.com/Alvin9999/new-pac/wiki/ss%E5%85%8D%E8%B4%B9%E8%B4%A6%E5%8F%B7)。

**第一种方法：**

ubuntu 安装 shadowsocks

***


用 PIP 安装很简单，

***

sudo apt-get update

sudo apt-get install python-pip

sudo apt-get install python-setuptools m2crypto

***

接着安装 shadowsocks

***

pip install shadowsocks

***

**如果是 ubuntu16.04 直接 (16.04 里可以直接用 apt 而不用 apt-get 这是一项改进）**

sudo apt install shadowsocks


***

当然你在安装时候肯定有提示需要安装一些依赖比如python-setuptools m2crypto ，依照提示安装然后再安装就好。
也可以网上搜索有很多教程的。

***

启动 shadowsocks

安装好后，在本地我们要用到 SSlocal ，终端输入 SSlocal --help 可以查看帮助，像这样

通过帮助提示我们知道各个参数怎么配置，比如 SSlocal -c 后面加上我们的 json 配置文件，或者像下面这样直接命令参数写上运行。

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/linus1.jpg)

请输入图片描述

比如 SSlocal -s 11.22.33.44 -p 50003 -k "123456" -l 1080 -t 600 -m aes-256-cfb

-s 表示服务 IP, -p 指的是服务端的端口，-l 是本地端口默认是 1080, -k 是密码（要加 ""）, -t 超时默认 300,-m 是加密方法默认 aes-256-cfb，

***

为了方便我推荐直接用SSlcoal -c 配置文件路径 这样的方式，简单好用。

***

我们可以在 / home/XX/ 下新建个文件shadowsocks.json (XX 是你自己电脑的用户名)。内容是这样：

{

"server":"服务器IP",

"server_port":远程端口,

"local_port":1080,

"paSSword":"密码",

"timeout":600,

"method":"aes-256-cfb"

}

***

server 你服务端的 IP

servier_port 你服务端的端口

local_port 本地端口，一般默认 1080

paSSwd SS 服务端设置的密码

timeout 超时设置 和服务端一样

method 加密方法 和服务端一样

***

确定上面的配置文件没有问题，然后我们就可以在终端输入 SSlocal -c /home/mudao/shadowsocks.json 回车运行。

如果没有问题的话，下面会是这样...

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/linus2.jpg)


如果你选择这一种请跳过第二种。你可以去系统的代理设置按照说明设置代理，但一般是全局的，然而我们访问 baidu,taobao 等着些网站如果用代理就有点绕了，而且还会浪费服务器流量。

我们最好配置我们的浏览器让它可以自动切换，该用代理用代理该直接连接自动直接连接。所以请看配置浏览器。

***

**第二种方法：**

安装 GUI 图形界面程序，然后按照提示配置相对应的参数。安装教程地址：[shadowsocks-qt5](https://github.com/shadowsocks/shadowsocks-qt5/wiki/%E5%AE%89%E8%A3%85%E6%8C%87%E5%8D%97) 安装指南

在 ubuntu 上可以这样，通过 PPA 源安装，仅支持 Ubuntu 14.04 或更高版本。

sudo add-apt-repository ppa:hzwhuang/SS-qt5

sudo apt-get update

sudo apt-get install shadowsocks-qt5


***


由于是图形界面，配置和 windows 基本没啥差别就不赘述了。经过上面的配置，你只是启动了SSlocal 但是要上网你还需要配置下浏览器到指定到代理端口比如 1080 才可以正式上网。

***

配置浏览器

假如你上面任选一种方式已经开始运行SSlocal了，火狐那个代理插件老是订阅不了gfwlist所以配置自动模式的话不好使。这里用的是chrome，你可以在 Ubuntu 软件中心下载得到。

***


安装插件

我们需要给 chrome 安装 SwitchyOmega 插件，但是没有代理之前是不能从 Google 商店安装这个插件的，但是我们可以从 Github 上直接下载最新版 https://github.com/FelisCatus/SwitchyOmega/releases/ （这个是 chrome 的）然后浏览器地址打开chrome://extensions/，将下载的插件托进去安装。


***


设置代理地址

安装好插件会自动跳到设置选项，有提示你可以跳过。左边新建情景模式 - 选择代理服务器 - 比如命名为 SS（叫什么无所谓）其他默认之后创建，之后在代理协议选择 SOCKS5，地址为 127.0.0.1, 端口默认 1080 。然后保存即应用选项。

***

gfwlist Github 更新地址：

https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt

**开机后台自动运行 SS**

**如果你选择了第二种可以不管这个**

如果你上面可以代理上网了可以进行这一步，之前我让你不要关掉终端，因为关掉终端的时候代理就随着关闭了，之后你每次开机或者关掉终端之后，下次你再想用代理就要重新在终端输入这样的命令 SSlocal -c /home/mudao/shadowsocks.json ，挺麻烦是不？


***


我们现在可以在你的 ubuntu 上安装一个叫做 supervisor 的程序来管理你的 SSlocal 启动。

sudo apt-get install supervisor

***

安装好后我们可以在 / etc/supervisor / 目录下找到 supervisor.conf 配置文件，我们可以用以下命令来编辑

sudo gedit /etc/supervisor/supervisor.conf

***

在这个文件的最后加上以下内容

[program:shadowsocks]

command=SSlocal -c /home/mudao/shadowsocks.json

autostart=true

autorestart=true

user=root

log_stderr=true

logfile=/var/log/shadowsocks.log

***

当然在 16.04 里你可以直接在/etc/supervisor/conf.d/下新建个文件比如 SS.conf 然后加入上面内容。

command = 这里 json 文件的路径根据你的文件路径来填写。确认无误后记得保存。

SSlocal 和 SSserver 这两个命令是被存在 /usr/local/bin / 下面的，我们要拷贝一份命令文件到 / bin

sudo cp /usr/local/bin/SSlocal /bin (注意空格)

**注意：16.04 命令在 /usr/bin / 下所以就用**

sudo cp /usr/bin/SSlocal /bin (注意空格)

***

现在关掉你之前运行 SSlocal 命令的终端，再打开终端输入 sudo service supervisor restart 然后去打开浏览器看看可不可以继续代理上网。你也可以用 ps -ef|grep SSlocal 命令查看 SSlocal 是否在运行。

***

这个时候我们需要在 / etc 下编辑一个叫 rc.local 的文件 ，让 supervisor 开机启动。

sudo gedit /etc/rc.local

在这个配置文件的 exit 0 前面一行加上 service supervisor start 保存。看你是否配置成功你可以在现在关机重启之后直接打开浏览器看是否代理成功。

ps：我对linus系统不懂，这是网上找来的教程，如果有什么问题，可以自己百度搜索一下。