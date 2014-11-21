---
author: admin
comments: true
date: 2010-12-10 03:55:21+00:00
layout: note
slug: jail-break
title: 折腾iPhone4, iPad越狱备忘录
wordpress_id: 3724
categories:
- 学点技术
tags:
- iPad
- iphone
- 技术指南
- 越狱
---

近来帮好友折腾iPhone、iPad无数，积累了一点心得，备忘如下。

1、越狱之前，先明确越狱目的不是为安装盗版软件，而是为了使用更好的输入法、更准确的地图，一句话为了更好的用户体验。而这些是高傲的苹果到死也不肯改变的。

2、先确认一下你的设备安装的iOS版本号（方法是：通用--设置--关于本机：找到版本，）如果是4.2.1以上，现在还没有完美的越狱方案。

3、如果iPhone版本是4.01-4.1，iPad版本是3.2.2及以下，恭喜你，可以完美越狱。

4、越狱之前，你需要先备份SHSH，需要用到的工具是小雨伞TinyUmbrella，每台设备都有独一无二的SHSH，不备份的代价就是，万一你升级到更高的版本，再也无法降级。

5、如果你升级到了4.2以上，可以用备份的SHSH降级。降级方法非常简单，尽管我重复摸索了好几天，坏的教程真是毁人不倦。

恢复SHSH的方法很重要，以下借鉴了[这篇英文文章](http://www.dkszone.net/downgrade-ios-4-2-1-4-1-iphone-43gs3g-ipod-touch-ipad)：

1）要有这台设备的.shsh备份，这个不需要去看隐藏文件夹，只要打开TinyUmbrella，就知道有没有备份。

1.5）然后要修改你电脑的hosts地址，把下面这句添加进去（这是用来欺骗苹果服务器的）：



<blockquote>74.208.10.249 gs.apple.com</blockquote>



在Mac上的修改hosts会报错，方法是hosts拖出etc文件夹，修改后放回去，覆盖即可

2）先打开TinyUmbrella,然后Start TSS server，并一直开到越狱结束。再打开iTunes.

3）你需要有你要降回版本的ipsw，这个可以搜到并下载。

4）按住POWER键3秒，POWER+HOME一起按10秒，松开POWER单按HOME，进入DFU模式。

5）这时候iTunes提示你要恢复，按着键盘的Alt键，用鼠标点“恢复”（或英文Restore），然后找到ipsw，恢复之。

6）中间iTunes要验证N次，我们开这TSS server，就是为了欺骗它的。否则苹果不允许我们降级。

7）装好之后，会出现一个错误，也就是1004错误。同学们不要紧张，只要拔线重启或者小雨伞点Exit Recovery就可以正常启动4.1了。


6、越狱方法，使用威锋网自制的绿雨越狱，具体方法，[请看这个链接](http://bbs.weiphone.com/read-htm-tid-1213345-page-1.html)。

7、越狱后安装威锋Cydia源，更换输入法。

8、iPhone建议使用百度输入法。

9、iPad的福音来了，搜狗输入法for iPad已经出炉，[具体安装方法请看这里](http://apple.zone.it.sohu.com/forums/thread-4248639-1-1.html)。刚才测试了一下搜狗输入法 for iPad 1.0版本，各种赞美，最棒的是集成了英文输入，所以只需要安装一个语言键盘就够了，再也不用在输入法键盘之间来回切换了。暂时只支持iOS 3.2.X。

10、强烈不建议安装太多cydia里的破解软件，很容易造成机器崩溃或者系统不洁净，所以，劝大家不要贪心。有了好用的输入法，大家应该知足。
