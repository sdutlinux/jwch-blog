---
layout: post
title: "日常工作"
date: 2012-06-16 12:50
comments: true
categories: group
---

先说下我们小组吧，我们小组现在有四个人，大一大四的都有，有一个带我们的老师。
服务器主要有两部分，第一部分是教学楼的监控，录播服务器等。第二部分在鸿远楼机房，是运行各种web网站。
## 三号楼情况
负责三号楼录播服务器的维护。操作系统是win 2003, 要做的是定期备份。每年暑假会对
三四五号楼的服务器，教室计算机统一的维护。

![3h](http://pic.yupoo.com/lidashuang/C2PSwxsR/medish.jpg)
![3h](http://pic.yupoo.com/lidashuang/C2PSwHlf/medish.jpg)

## 鸿远楼

简单说下第二部分吧。

有8台服务器和一台dell的磁盘柜，Dell的服务器居多，型号有R710和R510,其它的有浪潮，惠普的。

运行的服务主要是web服务器(nginx,apache,IIS)，数据库(mysql,oracle,sqlserver)等。网站比较杂。

操作系统有Red Hat,ubuntu server和windows 2003,所有的服务器都放在内网，使用端口转发或者反向代理访问。

比如我们网络教学平台，一台Dell R510运行的是网络教学综合平台 web 服务器(apache + tomcat) ,
数据库是oracle，运行在另一台服务器(Dell R710) ，这两台操作系统都是Red Hat(5.5和4.7)。
现在我们一般都用ubuntu server 。 因为网站比较杂，我们还会使用vmware server等，这样的
话新节省资源，备份也比较方便，试过xen server,还在感觉vmware server 方便一些。

在维护服务器

![server](http://pic.yupoo.com/lidashuang/C2PSwn1L/medish.jpg)
![server](http://pic.yupoo.com/lidashuang/C2PSw9tG/medish.jpg)

关于日常工作
先说说遇到过的主要问题吧

硬件问题，磁盘坏道，主板曝浆，内存等。
安全方面，服务器被入侵

最怕的是磁盘出问题，遇到过一次运行 oracle
的服务器磁盘坏道。当时是我和另外一名成员处理的，处理过程是这样的：
首先我们先尝试着导出数据，然后在一台测试机器上做测试导出的数据是否有效。如果数据已经损坏的话，只能用以前的备份。
还好导出的数据是有效的，因为我们之前没有oracle的经验，都是现学现做，做的时候比较小心，大约花了一个星期处理好。

现在我们服务器磁盘都做了Raid5，
数据比较安全。重要数据都会有自动备份。没有出现过数据丢失的状况。

安全方面，服务器都放在内网，有一台软路由做的防火墙，是用openwrt做的。自己写的iptables 规则，
对外只开放80端口。访问内网用端口转发，也会用nginx做反向代理 。没用防火墙之前，出现过一台
win2003被黑的情况。之后使用国产的海蜘蛛。由于海蜘蛛的各种限制， 这学期换成了openwrt .

做好备份，安全，工作量很小，平常其它时间都搞一些自己喜欢的技术。组织一交流活动.

鸿远楼有乒乓球室，可以轻松下。
![ping](http://pic.yupoo.com/lidashuang/C2PSwvWe/medish.jpg)

会组织一些技术交流
![part](http://pic.yupoo.com/lidashuang/BpvVnCXC/medish.jpg)
![part](http://pic.yupoo.com/lidashuang/BpvVpJBb/medish.jpg)
![part](http://pic.yupoo.com/lidashuang/BpvVrbgG/medish.jpg)
