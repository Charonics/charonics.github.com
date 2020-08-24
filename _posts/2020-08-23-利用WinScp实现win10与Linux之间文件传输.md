```
---
title: 利用WinScp实现win10与Linux之间文件传输
date: YYYY-MM-DD HH:MM:SS +/0800
categories: [系统, Linux]
tags: [Linux]     # TAG names should always be lowercase
---
```

##### 1、下载并安装好WinScp工具

下载地址：[WinScp](https://winscp.net/eng/docs/lang:chs)

安装过程按照流程来就行，没有什么坑，就不详细说过程了

##### 2、在win10的虚拟机上安装Linux系统

我使用的虚拟机是VirtualBox，软件就在官网下载按照提示进行安装就行。下面详细说一下安装Linux系统的过程。

点击新建

![image-20200824174300351](https://i.loli.net/2020/08/24/sCEMINKVw624JZa.png)

命名（随便取），根据自己要安装的版本选择

![image-20200824174417898](https://i.loli.net/2020/08/24/3pINo6mfYHTRyFh.png)

设置内存大小（自己根据实际情况选择就行）

![image-20200824174535123](https://i.loli.net/2020/08/24/q6u3gR9bcB2TemP.png)

依次进行下一步

![image-20200824174615981](https://i.loli.net/2020/08/24/MZVxNKd3hu7yv1Q.png)

![image-20200824174626572](https://i.loli.net/2020/08/24/DSTY6ChPONJFfcl.png)

![image-20200824174652276](https://i.loli.net/2020/08/24/s1iFhfZBqTOX8o3.png)

分配系统硬盘大小，点击创建

![image-20200824174801305](https://i.loli.net/2020/08/24/2mpMRSilB3zJAcD.png)

然后点击设置，在存储中在没有盘片哪里选择自己下载的系统的镜像文件，然后OK

![image-20200824175020548](https://i.loli.net/2020/08/24/bvcXjG71Up2tEmQ.png)

然后启动，选择启动盘，点击启动

![image-20200824181856073](https://i.loli.net/2020/08/24/4RL8j6QAtIJcwYE.png)

我装的Linux的发行版为Linux mint，如果你选择的系统是Ubtun等其他的发行版，那这里的操作应该就不一样了，选择start。

![image-20200824182107707](https://i.loli.net/2020/08/24/sfb6RiSBygNcdGZ.png)

之后点击安装就可以了，其实这里不用安装也是可以进行简单的体验的。

![image-20200824182522478](https://i.loli.net/2020/08/24/i3VlpnO7A48wY1d.png)

##### 3、接下来就是进行链接

主机名就是你Linux系统的IP地址，端口号默认就行，用户名和密码就是系统的用户名和密码。

![image-20200824192509347](https://i.loli.net/2020/08/24/ezLS7kpRaVXy1To.png)

不出意外的话便可成功链接，就可以进行文件传输了，可视化操作简单。

![image-20200824191945329](https://i.loli.net/2020/08/24/JnM6yxFdB5u8hm3.png)

如果链接不成功，有两种解决方式：

第一种是更改虚拟机网络链接设置：选择桥接网卡下的Adapter，这样虚拟机系统便可以和自己主机系统在同一局域网下，就可以连接成功了。

![image-20200824193208074](https://i.loli.net/2020/08/24/BVTFjuNbGQOli59.png)

第二种是在Linux系统中打开防火墙。这种方法我没试过，读者可以自行探索。