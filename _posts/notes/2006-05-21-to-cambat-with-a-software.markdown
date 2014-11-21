---
author: admin
comments: true
date: 2006-05-21 02:07:23+00:00
layout: note
slug: to-cambat-with-a-software
title: 你们不知道我有多么坚韧
wordpress_id: 6
categories:
- 学点技术
tags:
- 不好归类
---

周末在西湖边的Mashup Camp（捣浆糊会）上见到[Zheng](http://www.wangpei.net/home/content/r/e/d/redredpei/html/blog/wp-blog-header.php/www.klogs.org)。从去年开始，我一直追随他的脚步，他把虚拟主机放哪儿，我就跟着放哪儿。起先是[ ](http://www.wangpei.net/home/content/r/e/d/redredpei/html/blog/wp-blog-header.php/www.zhaomu.com)[](http://www.wangpei.net/home/content/r/e/d/redredpei/html/blog/wp-blog-header.php/www.klogs.org)[朝暮](http://www.wangpei.net/home/content/r/e/d/redredpei/html/blog/wp-blog-header.php/www.zhaomu.com)，后来很遗憾，那里提供的美国主机经常遇到风沙。这次见他，我迫不及待地想知道，他又搬到哪儿去了。

[Zheng](http://www.wangpei.net/home/content/r/e/d/redredpei/html/blog/wp-blog-header.php/www.klogs.org) 向我推荐了[GoDaddy](http://www.wangpei.net/home/content/r/e/d/redredpei/html/blog/wp-blog-header.php/www.godaddy.com)  ，我相信专家之选决不会错。连夜用信用卡花了50美元，买了空间，并注册了域名一枚。

正待我踌躇满志想安装WordPress的时候，忽然发现我犯了个错误，竟然看也不看买了Windows的主机。这事要搁咱们华夏，只好认倒霉了。但是这事发生在蛮夷之族，我决定发封信试试。说我希望换成Linux，并大量使用委婉语、疑问句和虚拟语气。
几个小时后，收到回信，客服说，他们的控制面板上就有这个功能，并做了详细说明。我连忙发了封感谢信，大量使用祈使句、惊叹号和过去将来进行时，没想到对方没空搭理我。

换回Linux，就装WP。一切还算顺利，兴高采烈写第一个帖子，结果我看到了一段致命的代码。

<strike>Your website has been censored and blocked.</strike>

幸好不是上面这段话，只要是技术问题，永远都是小问题。我虽文科出身，但曾经无数次跟技术玩命。踏过的尸体有：Redhat Linux，Writer's Blocks，Zblog，这个小贼能奈我何。

毕竟正业还是重要的，晚上跟同学拜会口语老师，手里的活停了下来。从老师家回来，我直奔办公室。搞不定这厮，我今夜根本无法入睡。

在WP的官方网站上，看到有[这样遭遇的人不止我一个](http://wordpress.org/support/topic/61425)。都是WP2装不上[GoDaddy](http://www.wangpei.net/home/content/r/e/d/redredpei/html/blog/wp-blog-header.php/www.godaddy.com) ，青丝愁成了白发。其中有个人说从96年就干IT，在无数夜晚跟无数难题斗争过，这次是几年来最痛苦的体验之一。

按照他们的指示，我把WP2装了删，删了装，好几次。最后都没有成功，还是发不了贴这个问题。


最后，我忽然明白：**也许我遇到的问题跟他们完全不一样！** 我仔细阅读了出错信息，发现，原来是有个文件找不到。怎么会呢？明明传上去了。我上FTP仔细比对后发现，服务器中的文件名是小写，本地是大写。

哦，我恍然记起，有一次我把LEAPFTP做了一个小设置，文件名强行改小写。**原来问题出在这里！**

当第一个test发布成功，我并没有特别激动。这是生活的一部分：遇到麻烦，求助，无助，自己想办法，直到解决。

感谢[Zheng](http://www.wangpei.net/home/content/r/e/d/redredpei/html/blog/wp-blog-header.php/www.klogs.org) ！感谢生活！感谢西湖边的[捣浆糊](http://www.klogs.org/2006/05/21/mashup2_hangzhou.html)！当然，我还要感谢自己！这是不能遗漏的。

** **
