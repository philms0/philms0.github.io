---
layout: post
title: IFTTT:Make Life Easier
date: 2014-12-14
author: Philms
header-img: “https://web-assets.ifttt.com/assets/home/new_home/above_ill_d-dd0b01e170eaa7d275357320c7c3b10000a00f34764b1ddc2d22842cb3cf383e.png”
catalog: true
tags: ["GTD","IFTTT","提醒","笔记"]
---

# IFTTT是什么

IFTTT 的全称为：**IF This, Then That，即 如果发生这个，那么就执行那个**。用户可以利用已经定义好的channel（目前IFTTT有153个channel）根据自己的需要完成所需操作：**即创建一个菜谱（Create a recipe），通过channel的特定事件进行触发(Trigger)，接着执行用户所选择的动作（Action**）。

折腾了近一个星期，终于将自己的一些想法做出来了，感觉这个App可以做一些轻量级尤其是重复和已经定义好的事情，辅助GTD简直是完美！（[关于智能手机、云端与GTD的思考：GTD RPG Cloud ](http://www.philms.info/2014-03/gtd-rpg-cloud/ "GTD RPG Cloud")）

# IFTTT的Recipe分类

根据功能，常见的Recipe分为以下几类：

## 社交同步

即同时关联你的各种社交帐号（支持的有新浪微博，Facebook，Twitter），当你在某个社交平台中发了个状态，则自动同步到其他社交平台；在某个平台上喜欢了一张图片，则自动将图片下载到网盘。（PS 通过添加微信公众号IFTTT，不用翻墙即可以实现将微信的图片和内容发布至Facebook，参见教程[微信IFTTT，用微信同步照片或信息到facebook和twitter。](http://www.zhaoyuhao.com/work/show/90)）

## 日常提醒

即通过判断明天的天气情况自动发送提醒：如明天降温啦，明天下雨啦，明天高温预警啦，则发送短信或者其他通知（由于中国地区无法使用短信业务，可以采用Notifacation或者下载Pushbullet达到同样目的）。

通过日期和日历进行提醒：信用卡账单，联系人生日，定期维护等（最完美、最节约精力的做法是将所有事件添加到Google Calender 然后只要Calender中事件触发则发送提醒）。

通过地理位置进行节约流量提醒：到家后提醒关闭数据流量，统计在公司的时间，发送某地的天气信息等。

某人博客更新了，某个物品降价了，App Store 限时免费 了，则发送提醒。

## 资料备份

将邮件附件自动保存到网盘（只支持DropBox Google Drive和OneDrive），将你的相册照片备份到网盘，将你的联系人备份至Google Spreadsheet等等。

# 一些想法

IFTTT理论上可以满足你的所有想法，前提是其他公司都能开放接口。现在可用的Channel已经有153个，我只用了其中的23个即可满足大部分需要了。

其实如果你有想法，善于利用Feed这一个channel 结合其他App如Pocket Evernote Onenote 网盘等等，都可以做出许多好玩的功能。举个例子，IFTTT没有Pinterest的接口，但是Pintererst的所有公开的board都是可以订阅Rss的，只要将Pinterest中喜欢的图片pin到指定的Board上，IFTTT就可以将这个图片的链接保存下来，剩下的就不说了。

## 一些用法举例

### 利用IFTTT下载软件

由于墙的存在，有些软件或者资料无法下载，这时候可以利用IFTTT服务进行远程下载；即建立recipe，发送链接至其指定邮箱，然后IFTTT会默认在后台进行下载并将文件发送到网盘；然后你需要登录网盘然后同步到本地即可。

### 将电子书推送到Kindle

在网盘下建立指定目录，若加入新文件，则自动发送到kindle邮箱从而推送到Kindle,

### 下载Bing的壁纸

微软的Bing每天会发布一张壁纸，只要一个Recipe即可将该照片自动保存到网盘

# 参考内容

#### [Channel List](https://ifttt.com/channels)

#### [知乎：哪些 IFTTT Recipe 大大提高了你的工作效率？](http://www.zhihu.com/question/20770508)
