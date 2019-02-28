---
layout:     post
title:      Wordpress2Markdown
subtitle:   将wordpress博客备份文件转为一个个md文件
date:       2019-02-27
author:     Philms
header-img: img/post/2017/post-bg-ios9-web.jpg
catalog: 	true
tags:
    - Wordpress
    - Markdown
    - js
---

### 将WP的全部文章xml备份文件转为一个个md文件

>之前的博客一直是在wordpress上。最近切换到GitHub后，每一篇博客都是一个文件，方便以后的管理。但是如何将之前的博客导入到GitHub成了困难。
>经过百度，找到了[解决方法](https://segmentfault.com/q/1010000007307027)。

#### 主要步骤

将Wordpress的博客文件导出，这个我之前已经导出了备份；

使用node.js的[wordpress-to-markdown](https://github.com/ytechie/wordpress-to-markdown)将其转换成markdown。

>注意我是在Windows平台做的，安装node.js后，运行convert报错，发现缺少xml2js和to-markdown模块。使用淘宝镜像cnpm安装这两个模块。

将wordpress的备份文件命名为export.xml，将其和convert.js放在同一目录下，打开cmd，执行node  convert.js会自动在目录中生成out文件夹，所有文章将按照【年/月/博客名称/index.html.md】的方式生成。

将生成的文件使用工具重命名为【年-月-日-博客名称.md】，再将这些文件放在_post目录下即可。

#### 另外一个未尝试的方法是使用[Python的wp2md](https://github.com/dreikanter/wp2md)
>此方法未做尝试，仅做备忘。
