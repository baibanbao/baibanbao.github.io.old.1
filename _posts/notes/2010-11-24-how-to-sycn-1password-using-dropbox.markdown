---
author: admin
comments: true
date: 2010-11-24 03:38:00+00:00
layout: note
slug: how-to-sycn-1password-using-dropbox
title: 1Password如何使用Dropbox同步
wordpress_id: 3583
categories:
- notes
- 学点技术
tags:
- mac
- 使用心得
- 正版软件
---

如果你不需要一个工具管理各种密码，那只有两种可能，一、你记忆力超好；二、你的密码太简单了。

1Password是[agilewebsolutions.com](http://agilewebsolutions.com)出的密码管理工具，有横跨Mac，PC，iOS设备的多个版本，结合Dropbox云存储，可以实现密码的跨平台同步和无痛管理。

赖 @justin7974 同学所赠，我现在拥有了一个1Password for Mac的正版使用权。

1Password在多种设备之间的同步，使用了两种方式，一种是WIFI，这个需要设备在同一无线局域网内，并且要用手动同步，非常不爽利。最方便的方式是通过Dropbox进行云同步。下面结合自己的经验，说说这种方式。

1、首先，你要有一个dropbox帐号，不对，首先你要飞跃长城，因为dropbox已经被墙认证过了，国内无法自动访问。如果你还没有帐号，可以通过[点这个邀请链接](https://www.dropbox.com/referrals/NTE5MTc4MDA5?src=global)申请一个，这样你和我的存储空间都会增加250M。

2、其次，你要安装Dropbox客户端，有Mac和PC不同版本，安装之后，在你的本地电脑上生成一个dropbox的文件夹。

3、MAC端的设置（PC设置类似）。

1）首先打开1password的“使用偏好”。找到第一项(中文界面请自行对号入座)，选择MOVE。

[![Screen shot 2010-11-24 at 上午10.23.38](http://farm6.static.flickr.com/5044/5203259704_0d68d5442c_o.png)](http://www.flickr.com/photos/42121485@N00/5203259704)

2）把1Password.agilekeychain从默认迁移到dropbox的文件夹。

[![Screen shot 2010-11-24 at 上午10.22.41](http://farm5.static.flickr.com/4152/5202664713_29f7f4a085_o.png)](http://www.flickr.com/photos/42121485@N00/5202664713)

这样就是实现了1Password与MAC/PC的同步了。

4、iOS端的同步。

本来以为这个会很简单，没想到，还有一个小陷阱，所以要介绍一下。

1）iOS安装了1Password客户端之后，在setting里，可以选择同步方式，强烈建议选择Dropbox同步。

[![IMG_0090](http://farm6.static.flickr.com/5041/5202639705_89c7eff542_o.png)](http://www.flickr.com/photos/42121485@N00/5202639705)

2）此时需要你添加你的Dropbox账户和密码，这个应该没什么困难。


3）问题在最后一步，等你的dropbox密码都添加完毕的时候，它让你再添加MAC和PC端的主密码。这主要是为了安全的需要，即，即便是有人破解了你的dropbox，不知道你的本地电脑端的Master Password，也无法阅读这些加密信息。

[![IMG_0098](http://farm5.static.flickr.com/4147/5202779713_a3f5544401_o.png)](http://www.flickr.com/photos/42121485@N00/5202779713)

这里有个小陷阱，当你本地电脑的主密码用了“shift+字符”的时候（例如含有@，%￥等等，按着shift输入的字符），在iOS设备上将被认错！从而提示你：主密码错误！目前的解决方法只有更改本地电脑主密码，只用大小写字母+数字。

总之，1Password是个管理密码的利器，但依然有一些BUG，使用起来需要一些耐心。而一旦你掌握了它之后，就再也离不开它，安心步入健忘的中年吧。
