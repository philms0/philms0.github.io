---
layout: 	post
title: 		无法打开博客图片和文档?
subtitle:	修改Hosts的方法
date: 		2014-10-01
author: 	Philms
header-img: img/post/2017/post-bg-ios9-web.jpg
catalog: 	true
tags: 		["Onedrive","Hosts"]
---

由于个人使用Skydrive-即Onedrive时间较长,且其容量满足要求,而博客空间有限,故而使用OneDrive保存所有共享的附件和图片.通过链接的方式访问所有图片和附件.

OneDrive网页版被DNS污染影响访问有段时间了，虽然OneDrive客户端可以正常同步，但对于和我一样使用OneDrive外链博客图片的朋友来说这无疑很不方便.
**对于大部分国人,需要使用代理或者修改Hosts才能访问部分内容.最为省心的方法是使用VPN,但是大部分VPN都是需要收费的,且要进行配置.所以免费修改HOSTS更为经济方便.**

现在大部分人都使用智能手机,为方便大家,特在此将Windows计算机,Mac和Andriod手机修改hosts的方法整理一遍.对于Iphone\WP及其它智能手机用户,貌似目前只能通过VPN解决.

# 修改Hosts的方法

## Windows 电脑

hosts 文件在以下目录:

**C:\Windows\System32\drivers\etc**

打开后添加如下代码
# One Drive
134.170.108.26 onedrive.live.com
134.170.108.152 skyapi.onedrive.live.com

Windows 7 及以上系统注意需要管理员权限

## Mac电脑

请执行以下程序

1.打开 应用程序--实用工具--终端

2.输入：sudo nano /etc/hosts

输入你的密码，打开Hosts后 添加

# One Drive
134.170.108.26 onedrive.live.com
134.170.108.152 skyapi.onedrive.live.com

3.编辑完毕之后按 ctrl+o 保存，出现 File Name to Write: /etc/hosts 的时候按回车确认，再按 ctrl+x 退出编辑。

## Andriod 手机

1.先通过各种方法让Android手机获取Root权限，之后运行Root Explorer管理器，进入可写状态，找到/system/etc/hosts的文件，将其权限修改为可写。

2.打开超级终端Terminal Emulator，输入su，进入root模式，输入 vi /system/etc/hosts 命令，按i进入编辑模式，之后将用户电脑上的hosts文件内容也输入进去。

# One Drive
134.170.108.26 onedrive.live.com
134.170.108.152 skyapi.onedrive.live.com

3.Android虚拟终端下当vi在编辑模式时，按下"确定"键（Trackball），再按下虚拟键盘上的"1"，就可以退出编辑模式了（CTRL+[），这个时候使用：wq就可以保存退出并重启手机。

## 祝愿大家顺利访问!

以下链接供测试

[大家看的设计书-笔记](https://onedrive.live.com/redir?resid=D4430E4D20DC72BF!3376&authkey=!AJS3Jo1zg4IGTfM&ithint=file,.pdf)