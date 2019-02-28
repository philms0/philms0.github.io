---
layout: 	post
title: 		树莓派打造NAS看片利器
subtitle:	教你一步步打造NAS看片利器
date: 		2014-11-02
author: 	Philms
header-img: img/post/2017/post-bg-ios9-web.jpg
catalog: 	true
tags: 		["NAS","SSH","树莓派"]
---

去年入手raspiberry pi ，因忙着找工作，没时间折腾，当时仅安装了XBMC功能-即当成机顶盒，利用HDMI或者黄色视频线将视频输出至电视屏幕，外接音响实现低端家庭影院功能。今年搬家后宿舍电视太差，放弃折腾。

最近发现手机容量太小，wifi信号不给力，又重新想起了Pi，搁置已久的NAS计划重新启动。
购买带电源的USB Hub -实现为移动硬盘和Pi供电，也可以为以后HMDI转VGA的线供电。
购买移动硬盘盒，装上之前拆下来的笔记本老硬盘，给Pi做共享用，多媒体资源可以直接从电脑拷贝至移动硬盘。（_主要是Pi的读写速度太慢，最高仅有4-5M/s,且宿舍无线网传输速度也只有不到2M/s。所以老硬盘完全够用，从电脑拷贝也比无线传输快。_）
将树莓派连上移动硬盘，移动硬盘和Pi均接到USB hub，Pi连上网线，硬件方面即完成。
下面为SSH连接树莓派进行相应设置

# 1.安装ntfs文件系统支持

本人主要从Windows电脑将硬盘视频拷贝至移动硬盘，播放高清资源，因此采用支持4G以上大文件的NTFS较好。
但是树莓派系统默认不支持NTFS，为此需要安装相应组件，其命令如下：

sudo atp-get update
#获取更新
sudo apt-get install ntfs-3g
#安装 NTFS文件支持

# 2.建立移动硬盘挂载路径

sudo mkdir /media/philms
sudo mount -t auto /dev/sda1 /media/philms
#先建立挂载路径，将移动硬盘挂载在该路径上
_备注：以上两行代码为手动加载，为实现自动加载，最简单的方法是利用sudo nano /etc/rc.local 将两行内容纳入
_

# 3.安装和配置 minidlna

sudo apt-get install minidlna
#安装 minidlna
sudo update-rc.d minidlna defaults
#实现 minidlna服务自启动
sudo nano /etc/minidlna.conf
#配置minidlna
**以下为摸索出来的配置**_
media_dir=V,/media/pi-philms/Video
# Video,Images,Music为移动硬盘文件夹名称
#<em>默认为media_dir=/media/pi-philms，将相应文件夹归类可以加快索引速度，而且minidlna是按照此处文件夹先后进行索引，推荐将大文件的文件夹放在最开始_
media_dir=P,/media/pi-philms/Images
media_dir=A,/media/pi-philms/Music
db_dir=/var/lib/minidlna
listening_ip=192.168.X.xxx
#此为树莓派IP
port=8200
presentation_url=http://192.168.X.xxx:8200/
#浏览器通过此地址查看minidlna状态
friendly_name=My-Pi
inotify=yes
notify_interval=600</em>

另外，配置和修改硬盘媒体文件后需要刷新，命令如下
sudo service minidlna force-reload
_**备注：由于树莓派的cpu和I/O较慢，因此可能索引文件花费时间较长，具体何时索引完成，可以通过浏览器查看其状态，而且如果没有更新文件的话少用此命令，不然每次都要索引半天**。_

# 3.安装DLNA播放器App

测试可使用DLNA的免费播放器有ACEPlayer和[VidOnPlayer](https://itunes.apple.com/cn/app/vidon-wan-neng-bo-fang-qi/id581454033?mt=8 "VidOn Player on iTunes"),但是好像播放MKV音频无声音，需要进一步摸索.

# 4.SSH客户端 远程控制树莓派

由于树莓派没有实体关机按钮，只能通过SSH进行关闭，因此需在手机端安装SSH客户端。在不需要使用时，通过手机远程关闭树莓派,再关闭pi和移动硬盘电源以减少发热和硬盘读写。

Over



2014-22-23 VidOnPlayer播放部分MKV文件无声音的解决方法，测试有效:

# [解决iPhone播MKV无声音问题](http://www.chinaz.com/news/2014/0813/363614.shtml "解决iPhone播MKV无声音问题")



