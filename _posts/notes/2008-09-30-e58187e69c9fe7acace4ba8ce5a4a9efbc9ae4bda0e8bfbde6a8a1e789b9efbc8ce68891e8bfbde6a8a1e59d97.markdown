---
author: admin
comments: true
date: 2008-09-30 15:50:12+00:00
layout: note
slug: '%e5%81%87%e6%9c%9f%e7%ac%ac%e4%ba%8c%e5%a4%a9%ef%bc%9a%e4%bd%a0%e8%bf%bd%e6%a8%a1%e7%89%b9%ef%bc%8c%e6%88%91%e8%bf%bd%e6%a8%a1%e5%9d%97'
title: 假期第二天：你追模特，我追模块
wordpress_id: 1714
categories:
- 学点技术
tags:
- Drupal
---

今天是放假的第二天，中午跟航标一起吃饭，聊起了某些网络建站商欺生与杀熟，就是把简单的东西说得特复杂，把免费的东西算作自己的，把不可或缺的部分拆成一个个模块，卖给客户，从而达到利润最大化。

为了不被痛宰，继续研究Drupal.

Drupal最骄傲的一点是它的扩展性，由于它是开源软件，很多程序员和爱好者开发了许多modules（模块），这类似于Wordpress的插件，但WP插件除了反垃圾留言的Akismet之外，都可有可无，Drupal的模块可不一样。没有模块，你住的只是一个毛坯房。

这个网站是模块的集散地（[http://drupalmodules.com/](http://drupalmodules.com/)），其中最重要的两个块是CCK和Views。因为Drupal提供的内容发布太简单了，根本无法适应网站的要求，所以需要CCK这个模块给予扩充。当然，每一个模块都不好掌握，你若有心，不必吃我这杯残酒，读一下这个小教程吧。《[CCK & Views 模块使用小结（Drupal6.x）](http://drupalchina.org/node/5087)》。

在安装模块的是，我发现一个问题，我安装的WAMP模拟环境总是报错：

`Fatal error: Maximum execution time of 30 seconds exceeded in ……`

这个问题是因为PHP做了响应时间的设定引起的，解决方法非常简单，可以一劳永逸。
打开：sites/default/settings.php
加入这一行代码：
`ini_set('max_execution_time', 0);`

加到哪儿？这个问题真笨，你搜索一下ini_set，加在这一串后面就可以了。
