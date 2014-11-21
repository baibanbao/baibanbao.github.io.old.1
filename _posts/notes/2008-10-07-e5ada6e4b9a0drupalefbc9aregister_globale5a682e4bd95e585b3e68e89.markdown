---
author: admin
comments: true
date: 2008-10-07 17:41:16+00:00
layout: note
slug: '%e5%ad%a6%e4%b9%a0drupal%ef%bc%9aregister_global%e5%a6%82%e4%bd%95%e5%85%b3%e6%8e%89'
title: 学习Drupal：register_global如何关掉
wordpress_id: 1722
categories:
- 学点技术
tags:
- 技术 drupal
---

如果你在虚拟主机上安装drupal，很可能会遇到一个烦恼。安装的时候，出现一行提示，意思是说，你的php配置有问题，register_global是enabled，要求你把它turn off.

这个任务不可能完成，因为主机提供商不会因为你一个客户，把这个变量给关掉。那么怎么办呢？以下办法通常是有效的。

1、打开.htaccess这个文件；

2、在任何地方加入这一行代码：

`AddType x-mapp-php5 .php `

3、OK

至少在我的空间上所作的测试是成功的。

对不起，今天我又在聊技术。
