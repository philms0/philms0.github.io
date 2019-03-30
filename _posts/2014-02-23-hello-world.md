---
layout: 	post
title: 		Word Press博客建立笔记
subtitle:	一步一步搭建自有域名博客
date: 		2014-02-23
author: 	Philms
header-img: img/post/2017/post-bg-ios9-web.jpg
catalog: 	true
tags: 		["Word Press","博客","笔记"]
---

_ 建立自有域名的博客是本人2014年的年度计划之一 - **本命年总要做点让自己人生有意义的事情！**_

# Embrace Change and Make a Difference !

_ 第一次建立自有域名的wordpress 的博客，花费了好几个小时，汗！为了方便以后的操作，将此记录在此，作为第一篇博客。_

建立之前参照了[知乎](http://www.zhihu.com/question/19594033?rf=19900824 "怎样搭建一个自有域名的 WordPress 博客？")帖子中的一些内容，在此表示感谢！

# 1.购买域名

在[goDaddy](http://www.godaddy.com/ "GoDaddy域名购买")中搜索需要购买的域名（支持支付宝且），为了方便支付和对价格进行判断，可以将在页面左上角将汇率设置为CNY(￥)，这样你就能知道他的域名大概多少RMB而不是美元了。至于购买和注册这些和正常购物差不多，略去。

# 2.购买主机空间

安装里面的推荐，选择了老薛主机，按照自己的需求选择了相应的主机大小。记得在付款的时候输入10off就可以有9折优惠。

# 3.域名解析

这个是折腾我最久的地方，一开始老是无法访问我自己的网站。最后参考了[GoDaddy域名解析教程](http://www.lcjcl.com/post/18ad18_7c9c80 "GoDaddy域名解析教程")以及知乎中关于DNSPod的内容才完成。步骤如下：
获取自己主机空间的IP，将其在goDaddy中的DNSzone中奖里面的68.178.×××.100 改成自己的主机空间IP
在DNSpod中注册并将自己的域名进行解析（记得添加www和@ 两个解析，否则网站可能无法正常访问）
在goDaddy中的NameServer改成DNSPod的，即f1g1ns1.dnspod.net 和f1g1ns2.dnspod.net

# 4.安装WordPress

由于域名解析的问题，我采用网上的自己安装WP的方法无法完成，最后采用主机空间中提供的Wp的installation完成。

# 5.对WP进行优化

## 安装主题

安装自己喜欢的主题-经过一个月的折腾，最后选择了比较简约的MetroBlog（by the [The Smart Magazine Themes](http://smthemes.com/ "Visit author homepage")）作为我的主题

## 安装插件

安装一些必要的插件，已安装的插件有

### Add Post URL

在博客顶部和底部添加一些文章版权和其他信息

### Akismet

用来防止垃圾邮件

### Open Social for China

添加国内的社交网站分享图标--感觉不是很实用

### Simple URLs

添加短链接-感觉用处不大

# >关于使用Skydrive中的图片作为博客引用

由于主机空间大小只有300MB，如果发布图片博客的话，不到几天可能容量就会告急。经过搜索，发现可以使用Skydrive（现在叫OneDrive），而我的SkyDrive还有7G的空间，足够用来发布图片了。

基本方法为-登录skydrive-将图片upload到公共文件夹，找到想要使用的图片，点击图片，查看原始版本，复制图片链接，在WP中插入即可。感谢[风格范儿](http://www.stylefanr.org/archives/628 "太简单了！用SkyDrive做免费图床")博文的帮助！(_批量上传图片的方法还没找到,目前还是单张,略微花费时间_)

[![Screen shoot of my blog]](https://philms.today/)]

## 备注

之前使用的方法如下：但是其缺点是图片在IE中打开过慢，且不是原尺寸大小，故放弃
基本方法为-登录skydrive-找到想要使用的图片，点击嵌入，在弹出的页面中复制代码就行。（注意粘贴的时候需要切换到text模式，测试成功） 。感谢博客[the Blog](http://lemolu.com/?p=56 "使用window skyDrive嵌入图片到wordpress")-[amuseme ](http://lemolu.com/?author=1 "Posts by amuseme")的帮助！

_2014-04-01补充经过n次折腾，最后选择了MetroBlog主题，比较满意，不再折腾。以后安心写内容!_

______________________________________________________________________________________
_Update:2014-09-17_

# 解决博客访问慢的问题

之前一直不知道是主题的原因，导致博客访问特别慢，半天无法加载。一直拖延......在忍受约半年后台和博客访问龟速之后，终于下定决心解决这个问题。经过几天的Google和[知乎](http://www.zhihu.com/question/24104509#answer-5989258 "博客加载慢")，找到解决方法如下：

博客加载慢的原因是主题调用了一些Google的服务，这个也可以从博客打开左下角的信息反映出来；

找到原因之后就好办了，将博客主题文件中的相关代码进行替换，重点是Google CDN服务和jQuery库；

安装"Disable Google Fonts"插件即可解决后台访问缓慢问题；

替换Google iQuery库（我用的是MS 的）；

最后的重点是主题调用的Google地图，这个是罪魁祸首，解决方法-将Google 改成Baidu，估计这个功能是废了，暂时先这么着吧，以后有需要再继续研究！

______________________________________________________________________________________
_附上之前写的为什么要开通博客的缘由_

# 我为什么要开通博客

_Date:2012-08_

## 「你关注的东西决定了你」

织围脖也有一年多了，但是基本上潜水更多，关注的东西也是碎片化，感觉人都变得更加浮躁、焦虑。而且关注的东西确实会或多或少地在改变自己。

## 「人来到世界上总要做点有意义的事」

换到新地方也有一个多月了，来到新城市总要作出一点改变，而且这期间实发生了几件对我影响比较大的事情，让我重新思考我自己-「我的目标、我的未来」‎。

原来考研的目的都忘得差不多了，还好现在又想起来了。因此，我要作出一点改变。

开通博客，记录想法，整理思路；写下点滴，留下当初的自己！