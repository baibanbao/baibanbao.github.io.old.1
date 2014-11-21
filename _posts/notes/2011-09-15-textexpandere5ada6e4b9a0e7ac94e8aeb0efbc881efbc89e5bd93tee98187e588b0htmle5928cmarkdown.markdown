---
author: No Content Found
comments: true
date: 2011-09-15 17:10:40+00:00
layout: note
slug: textexpander%e5%ad%a6%e4%b9%a0%e7%ac%94%e8%ae%b0%ef%bc%881%ef%bc%89%e5%bd%93te%e9%81%87%e5%88%b0html%e5%92%8cmarkdown
title: TextExpander学习笔记（1）当TE遇到HTML和Markdown
wordpress_id: 6559
categories:
- notes
- 不好归类
---

希望有一天我也能象小欠一样写出[OmniFocus教程](http://tumblr.com/xuz4o3y1ng)一样，写出一个TE的教程。当然，那前提是我自己要应用得烂熟于心才行。





现在还不成，还需要继续操练。以下即为操练笔记。





一、当HTML遇到TextExpander





TextExpander与html结合应用一例。





插入图片，可以定义一个缩写snippet，比如：iimg，令其替代下列字符串：





`<img src="%fill:url%" alt="%fill:image description%" width="%fill:width%" height="%fill:height%" border="%fill:border%" align="%fill:alignment%" />`





这样，你只要输入iimg，就会跳出下面的输入界面：





![](http://media.tumblr.com/tumblr_lrkpz0uR5W1qz6vj8.png)





贴入你要链接的图片的url，其余可以填，也可以留空，这样岂不很方便吗？





二、当Markdown遇到TextExpander





看到这里你马上想到了，既然TextExpander可以跟html相结合，为什么不能跟Markdown相结合呢？





你真聪明，事实上，TextExpander与Markdown可以建立珠联璧合的关系。





比如加链接：





我们可以定义一个snippet,比如说叫llink，将其赋值为：





`[%fill:Link Words%](%fill:url%)`





输入之后，就会出现这样一个界面：





![](http://media.tumblr.com/tumblr_lrkqcbBswg1qz6vj8.png)





我们在里面分别输入：一般般，和1banban.com，就生成下面的Markdown语句。





[一般般是个好网站](http://www.1banban.com)
