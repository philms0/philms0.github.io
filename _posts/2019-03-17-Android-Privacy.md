---
layout:     post
title:      安卓手机的隐私管理
subtitle:   解决安卓手机的隐私泄漏的一些方法
author:     Unkown
date:       2019-03-17
header-img: img/post/2017/post-bg-ios9-web.jpg
catalog: 	true
tags:
    - 安卓
    - 隐私
---
[![这是一个视频测试]()](http://124.14.19.182/65728774E653E7191D171234D/03000A01005CA1859095C4F309744B72C8F450-2011-42EF-A1D7-792BC5A4D35E.mp4?ccode=0519&duration=170&expire=18000&psid=5a3ac7d96eb7054223c050e63e3ba8c5&ups_client_netip=daf92d42&ups_ts=1554111338&ups_userid=&utid=LZLZDe4T3CcCAdr5LULv5yeF&vid=XNDEyMDk1MTA3Ng&vkey=A87977b62e465eb34426b62abd8653beb&s=bbeb2ecefd644b98b778&sp=&ali_redirect_domain=vali.cp31.ott.cibntv.net&ali_redirect_ex_ftag=168683dcfee8332980c0fa2635eae10318962371d07af50f&ali_redirect_ex_tmining_ts=1554111339&ali_redirect_ex_tmining_expire=3600&ali_redirect_ex_hot=0)

重新使用LineageOS刷机

目前是LineageOS加Gapps，只在Google Play, F-Droid以及Github下载应用，非以上来源的应用一律安装到Shelter。

用App Ops管理国内应用的权限，不影响使用的都拒绝，例如微信只给相机、存储和剪贴板，支付宝只给相机，

用绿色守护管理应用的后台活动，国内的应用一律绿色化，无视了background-free和running state，

在F-Droid下载ClipboardCleaner管理剪贴板。

最后两点说明：安装Xposed加XPrivacyLua应该能将应用权限限制得更彻底，大部分应用哪怕在App Ops拒绝了所有权限也还能运行，但有一些......比如虾米，必须要给存储权限才能使用，可以使用Storage redirect来实现。
