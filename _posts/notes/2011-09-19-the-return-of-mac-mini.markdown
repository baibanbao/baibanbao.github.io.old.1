---
author: admin
comments: true
date: 2011-09-19 21:24:17+00:00
layout: note
slug: the-return-of-mac-mini
title: Mac Mini王者归来记
wordpress_id: 4804
categories:
- notes
- 各种工具
---

自从[Mac Mini被我弄坏](http://wangpei.info/post/10096150865/the-birth-of-a-tragety)之后，我度过了假装世上没有它的十天。





昨天打电话给果硕维修中心，他们说不但更换被我弄坏的i/o接头，还帮我换了ssd硬盘（型号：crucial m4 256g），但是不确定有没有修好，因为他们没有显示器，无法测试。我赶紧背着显示器出门，钱包里装了不多不少正好1000元钱，准备在对方狮子大开口的时候，掏出钱包给他们看，“就这些钱，再多，没有了，大不了，我mini不要了。”结果，他们只收了我200元钱，感动死了！





由于原装系统盘已经拆掉，新的ssd需要重新安装系统，我用了[Carbon Copy Cloner](http://www.bombich.com/)这个软件，事先把原来的硬盘克隆备份出来。安装过程非常简单，用移动硬盘启动之后，再用Carbon Copy Cloner还原，整个过程大约用了40多分钟。





不过，这一切并没有让我很高兴，因为启动速度很慢，根本不像人们传说的那样，如飞如电。我用秒表测了一下：







  * 关机：5秒，正常，可以接受。


  * 从按开机电源到开机完成：52秒。





这甚至不如我没有换ssd之前，那时测的启动时间只要35秒。





我用Google寻找原因与解决方案。出于对中文内容的不信任，我都用英文搜索。关键词是：“mac mini ssd installed boot speed slow”。





结果让我欣喜地发现，[有人遇到过跟我一样的问题](http://forums.macrumors.com/archive/index.php//t-691709.html)。这就好办了，我认真地读完这个帖子，对着夜空一阵无声地大笑。原来解决方法如此简单：





进入Preference（设置）－－start disk（启动盘），可以看到，硬盘在那里，但是没有被选中和加亮。





![](http://media.tumblr.com/tumblr_lrsglc04sb1qz6vj8.png)





选中它，然后点Restart（重启）。





奇迹发生了！启动时间从52秒，减少到17秒！





这才是ssd的魅力之所在！





至此，我的Mac Mini 2011款正式王者归来！



