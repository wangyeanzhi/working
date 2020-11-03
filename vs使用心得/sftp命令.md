

**首先要先确定那个是远程那个是本地？**
sftp是登录到远程，那个服务器就是远程，本地pc就是本地。</br>
get和put都是相对于*本地*来说的，get得到，就是从远程下载，put推送，就是从本地推到远程服务器。</br>

再就是，操作远程的服务器命令和linux中的一样，若操作本地的则多加一个l。


1. 登录
``` bash
#密码登录
sftp -P 22 zhangsan@192.168.0.100
#秘钥登录
sftp -P 22 -i ~/.ssh/id_rsa zhangsan@192.168.0.100
```

2. 更改远程工作目录
```bash
cd /abc
```
3. 更改和/或打印本地工作目录
```bash
lcd /abc
```

4. 列出远程目录的内容
```bash
ls
```

5. 列出本地目录的内容
```bash
lls
```
6. 打印远程工作目录
```bash
pwd
```

7. 打印本地工作目录
```bash
lpwd
```

8. 浏览您的本地目录，即打开本地目录
```bash
explore
```
9. 将文件从服务器下载到本地计算机
```bash
#把sftp服务器上test.txt文件下载到本地
get /tmp/test.txt ~/
#把sftp服务器上test文件夹下载到本地
get -r /tmp/test/ ~/
```

10. 将文件从本地计算机上载到服务器
```bash
#把本地文件test.txt上传到ftp服务器/tmp目录下
put ~/test.txt /tmp/
#把本地文件test上传到sftp服务器/tmp目录下
put -r ~/test /tmp/
```

11. 在远程服务器上创建一个目录abc
```bash
mkdir abc
```

12. 移动或重命名远程服务器上的文件
```bash
mv /test.txt /abc.txt
```

13. 移动或重命名远程服务器上的文件
```bash
rename /test.txt /abc.txt
```

14. 删除远程服务器上的文件abc.txt
```bash
rm abc.txt
```

15. 删除远程服务器上的目录abc
```bash
rmdir abc
```
16. 给予帮助
```bash
help
```

17.  清屏
```bash
clear
```

18. 完成您的SFTP会话，即断开连接
```bash
bye、exit、quit、!
```


























