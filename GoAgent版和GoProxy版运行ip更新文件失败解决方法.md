运行ip更新文件受阻时，即出现“无法找到文件”字样，多半是杀毒软件在起干扰作用，这个时候把杀毒软件退出来，然后重新解压再运行ip更新文件，ip更新文件有两个ip-1和ip-2，更新内容一样，都可以尝试。

如果已经排除了杀毒软件的影响后还是无法正常更新，使用GoAgent版时请检查Agent文件夹里面是否有名为proxy.user.ini_backup文件，如果没有，请自行建立一个文件，方法是复制proxy.user.ini并粘贴在Agent文件夹里，然后改其名字为proxy.user.ini_backup即可。记住一定要保证Agent文件夹里面有proxy.user.ini和proxy.user.ini_backup两个文件。
如图：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/ip.PNG)


使用GoProxy版时请检查Agent文件夹里面是否有名为gae.user.json_backup文件，如果没有，请自行建立一个文件，方法是复制proxy.user.ini并粘贴在Agent文件夹里，然后改其名字为gae.user.json_backup即可。记住一定要保证Agent文件夹里面有gae.user.json和gae.user.json_backup两个文件。


如图：

![](https://raw.githubusercontent.com/Alvin9999/pac2/master/ip2.png)


***

如果按照上述方法还是没法正常更新，请联系邮箱kebi2014@gmail.com


