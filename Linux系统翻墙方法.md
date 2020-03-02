**2020年3月2日更新，增加v2ray使用方法。**

### 第一种方法：使用SSR账号翻墙

[Linux客户端一键安装配置使用脚本(使用方法见注释)](https://github.com/the0demiurge/CharlesScripts/blob/master/charles/bin/ssr)
[Linux SSR 使用方法二](https://github.com/Turing2333/Detailed-tutorial-on-the-building-and-usage-of-SSR/blob/master/Instructions/Clients%20manual%20for%20each%20platform/Linux%20SSR%E7%9B%B8%E5%85%B3%E8%AF%B4%E6%98%8E.txt)

[全平台SS/SSR客户端下载汇总](http://www.mediafire.com/folder/sfqz8bmodqdx5/shadowsocks相关客户端)

[获取最新SS或SSR账号](https://github.com/Alvin9999/new-pac/wiki/ss%E5%85%8D%E8%B4%B9%E8%B4%A6%E5%8F%B7)
 

### 第二种方法：使用v2ray账号

**1、准备**

在这里下载适合系统的压缩包，并解压到 ~path/v2ray文件夹中。

编辑config.json配置文件，略。。。


**2、配置**

将v2ray文件夹移动到 /usr/local/目录下，然后进入该目录

  sudo mv /home/jacen/Downloads/v2ray /usr/local/v2ray

  cd /usr/local/v2ray/

创建配置文件目录 sudo mkdir /etc/v2ray

将配置文件复制到刚才创建的目录 sudo cp config.json /etc/v2ray/

运行v2ray

  cd /usr/local/v2ray/

  sudo ./v2ray --config=/etc/v2ray/config.json

**3、设置开机启动**

执行以下命令，修改启动脚本

  cd /usr/local/v2ray/systemd/

  sudo vi v2ray.service

将里面的ExecStart键值改为下面的 /usr/local/v2ray/v2ray -config /etc/v2ray/config.json

保存退出。


将文件复制到服务目录。 sudo cp v2ray.service /lib/systemd/system/

启动服务并开机自启

  sudo systemctl start v2ray.service

  sudo systemctl enable v2ray.service

停止服务 sudo systemctl stop v2ray.service

关闭开机自启

sudo systemctl disable v2ray.service

**注意事项**

关于配置文件，如果有win系统版的V2rayN软件，并成功配置了的，可以直接将其导出，替换压缩包里面的文件，不用修改即可直接使用。

代理设置应该和配置文件中保持一致

[获取最新v2ray账号](https://github.com/Alvin9999/new-pac/wiki/v2ray%E5%85%8D%E8%B4%B9%E8%B4%A6%E5%8F%B7)

***

有问题或者有更好的Linux软件分享，都可以发邮件到海外邮箱进行反馈kebi2014@gmail.com