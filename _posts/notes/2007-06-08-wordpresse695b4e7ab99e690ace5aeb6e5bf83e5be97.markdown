---
author: admin
comments: true
date: 2007-06-08 20:35:05+00:00
layout: note
slug: wordpress%e6%95%b4%e7%ab%99%e6%90%ac%e5%ae%b6%e5%bf%83%e5%be%97
title: Wordpress整站搬家心得
wordpress_id: 1041
categories:
- notes
- 学点技术
---

民间说，若想一个月不肃静，搬家。Wordpress搬家这件事如果搞不好的话，会变成一件劳心劳力的大烦恼。从昨天到现在，我在12个小时之内断断续续，终于把Wordpress连同数据库一起，从一个服务器搬到了另一个虚拟主机，没有遇到江湖中盛传的乱码问题。皆因文科生阅读能力强，喜欢下力气看帖子，读文档。

先简要介绍一下技术参数。我装的WP是Wordpress2.2，两边的数据库都是MySQL4.0+，托管商提供的数据库管理界面是phpAdmin，我想大多数虚拟主机都是这样。

在搬家之前，我看了好多帖子，尝试了多种方法，都没有成功。为了节约大家时间，我就直奔主题，介绍一种最简洁有效的办法，这一办法继承了[张翼轸介绍的方法](http://blog.earlzhang.com/others/140/)，再加上自己的一点心得。

假设你有两个博客，一个a.com，一个b.com，你想把a站的全部内容连同数据库迁到b站。OK,跟我来。

1、装WP程序：首先你要确保b.com已经装上了Wordpress，数据库里有没有内容都无所谓，反正一会要被洗掉的。

2、装WP插件[WP-DBManager](http://www.lesterchan.net/wordpress/readme/wp-dbmanager.html)：在a、b两个站点都装上一个Wordpress插件：[WP-DBManager](http://www.lesterchan.net/wordpress/readme/wp-dbmanager.html)。注意，只有用这个插件最管用，很流行的那个数据库备份插件不好使，直接到phpAdmin倒腾，非我等菜鸟力所能及。





<blockquote>2.1 这里罗嗦一句，[WP-DBManager安装](http://www.lesterchan.net/wordpress/readme/wp-dbmanager.html)分两步走，第一步，先把DBManager这个文件夹传到你网站的wp-content/plugins里，然后激活插件；第二步，这时用FTP登陆你的网站，看wp-content目录下，应该增加了一个子目录backup-db，把压缩包里.htaccess这个文件传到wp-content/backup-db目录里。OK。</blockquote>





3、备份数据库：好了，现在到a.com的管理界面，你会发现顶部的工具条里多了一项Database，这就是DBManager的功劳。点Database，出来一排菜单，点第二项”Backup DB“。 基本可以傻瓜操作，记得最后一项，GZIP Database Backup File?是问你压不压缩，默认是NO。你要选YES。要知道SQL文件压缩与不压缩大小相差四五倍。

4、管理备份的数据库：这时好奇心会驱使你看第三项菜单Manage Backup DB。你会看见，刚才备份的数据库列在一个表里，右侧是个可选的圆点小按钮。像这样：





<blockquote>fuxgfws.sql.gz（举例）   Friday, 8th June 2007 @ 13:21	  3 MB</blockquote>





下面什么E-mail database backup的不用去管它。注意：fuxgfws.sql.gz就是你备份下来的数据库压缩文件，它在哪儿呢？有才的你一猜就知道，在a站的wp-content/backup-db目录里。

5、FTP转数据库：FTP登陆到a.com，把wp-content/backup-db目录里的fuxgfws.sql.gz（举例）拉到本地来，然后再FTP登陆b.com，同样的把fuxgfws.sql.gz（举例）传到b站的wp-content/backup-db下。清楚吗？

6、恢复数据库：好现在进入b站的Wordpress管理界面，进入Database-->Manage Backup DB，你会看到fuxgfws.sql.gz在列表里了，点右边的圆点，选中，然后点下面四个按钮中的第二个Restore。会跳出一个警报标志，罗里罗嗦说一堆，不用管它，按确定。

7、奇迹出现了，但是……你会发现a站的内容已经顺利导入了b站，但不要高兴的太早。如果你换了域名的话，你会发现，b站所有的链接都是a站的，包括管理界面都会进入a站。这不是爱丽丝漫游奇境，原因很简单，数据库里有个重要的表内容还是a站的。没办法，我们必须用phpAdmin了。

8、根据你托管商给的登陆ID口令，找到MySQL管理按钮，最终进入phpAdmin管理界面（我的管理端是phpAdmin2.6.4，嘘，小声点，敏感词汇）。答应我，做两件事：

8.1 第一把咱们的孩子拉扯大……不胡扯了。第一，把phpAdmin的语言从默认的Chinese Simplified zh-gb2312 给我换成 Chinese Simplified zh-utf-8，达人们谆谆告诫，可以防止乱字符。听人劝，吃饱饭。

8.2 在左侧的一串辛德勒名单中找到 wp_options，点击进入，再点浏览（有时鼠标放上去才会出现“浏览”二字），不管怎么说，你要找到这个表，其中：

option_name这一列，下面一行写着	siteurl
往右 option_value这一列，下面写着一个网址，对了你会发现它就是你a站的网址，比如说：a.com

8.3 剩下的你应该会做，在这一行前面有个小钢笔的图标，那是编辑标志，点它，把a.com换成现在的b.com，保存。好了。不过距离革命成功还差一步。

9、WP管理界面修改选项。现在你发现，b.com的管理界面已经可以登陆了。进入后，找到选项，把Blog address (URL):换成b.com就行了。

蕾丝我也，下课。
