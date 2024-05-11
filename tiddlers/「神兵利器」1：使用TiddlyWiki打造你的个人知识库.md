**碎片化的学习，需要一个『碎片化』的笔记本。** 

**01**
------

成年人的世界，只有碎片化的个人时间。随之而来的，就是碎片化的学习。坐地铁时刷到的一些金句，工作间隙看到的好点子，大脑闪过创造性想法，都值得收集。

君子善假于物也，我们都需要一个信息管理系统。

我尝试了很多工具，手账、大本子、手机备忘录、各种软件，发现都不是很适合碎片化场景。直到我发现了一个神兵利器——TiddlyWiki。

TiddlyWiki是一个基于网页的“非线性笔记本”，可以『随身携带』，它不属于任何公司（不用担心公司倒闭）。它可以实现很多强大的功能，最核心的就是，它就像一个个人的维基百科，支持笔记间的链接与跳转，除此之外，支持图形、数学公式、各种Markdown排版等。你的想法，你记录的东西都可以放在一起，随时可以检索出来。

当然，还可以把它当做个人博客用。一般的，搭建博客需要购买服务器，域名，还需要一定的建站技能，同步代码等，现在你可以get一个免服务器、免域名（甚至可以取一个靓气的域名，当然是在[http://github.io](https://link.zhihu.com/?target=http%3A//github.io)下面）、免同步的TiddlyWiki笔记本了。

TiddlyWiki官网：

一个玩家的wiki页面：

**02**
------

TiddlyWiki虽然好用，但是需要一定的折腾打造能力。我周末用了两天时间，试着将其搭建到我的群晖服务器上，结果发现内网映射很麻烦，速度还很慢。

想起我之前在Github上搭建了一个hexo博客，研究了一下，发现可行。但是我发现，中文网上居然没有相关的博客介绍如何利用免费的Github Page服务搭建一个个人TiddlyWiki，于是有了此文，分享我的方法，让更多小伙伴享受这一神兵利器。

步骤清单：

1.  申请GitHub账号
2.  创建一个仓库
3.  生成Page页面
4.  将TiddlyWiki上传至仓库
5.  申请token，配置TiddlyWiki

03
--

1、申请Github账号
------------

很简单，不赘述

2、新建仓库
------

仓库名命名为\[username\].[http://github.io](https://link.zhihu.com/?target=http%3A//github.io)，其中username为你的GitHub用户名，比如我的用户名为mywiki，我的仓库名需要命名为[http://mywiki.github.io](https://link.zhihu.com/?target=http%3A//mywiki.github.io)，这样做的好处就是让你可以使用\[username\].[http://github.io](https://link.zhihu.com/?target=http%3A//github.io)链接来访问你的TiddlyWiki页面。

若仓库名命名为其他， 需要使用\[username\].[http://github.io/](https://link.zhihu.com/?target=http%3A//github.io/)仓库名。比如我的仓库名设为wiki，我要通过\[username\].[http://github.io/wiki](https://link.zhihu.com/?target=http%3A//github.io/wiki) 来访问，多了一个后缀，就不酷了。

3、生成Github Page
---------------

Page是Github官方免费给用户提供的一个静态页面站点工具。

最新做法，参照Github官方做法：

4、将Tiddlywiki模板上传到仓库
--------------------

你需要下载一个空白的中文简体模板：

打开上面这个网页，鼠标右键另存为一个html的文件。

你也可以拿来主义，把你喜欢的Wiki页面直接保存为HTML，作为一个冷启动策略。

上传至仓库有个小技巧，你不用会git命令，直接在GitHub仓库下新建一个HTML文件，可以命名为index.html（其他任意名字均可），后面会用到。

将下载得到的html文件，用记事本或者其他文本编辑软件打卡，内容全选，复制，再粘贴到仓库的新index.html文件里面，保存即可。

在Page设置里面，将page解析页面设置为这个index.html（默认为readme.md）。

5、申请Token，配置TiddlyWiki
----------------------

参照Github官方指引申请token ，其实就是一个很长的密码，可以用于修改GitHub仓库里面的文件，实现TiddlyWiki的修改功能。

权限可以全部都选择，申请好token后，新开浏览器标签页打开网址\[username\].[http://github.io](https://link.zhihu.com/?target=http%3A//github.io)，点击「设置-保存-GitHub保存模块」,按照如下方式填写。

| 项目 | 内容 |
| --- | --- |
| 用户名称 | 填写你注册的GitHub用户名 |
| 密码、OAUTH 令牌，或个人存取令牌 (详见 GitHub 帮助页面) | 填写你申请到的token |
| 目标存储库 | 填写你的仓库，即\[username\]/\[username\].[http://github.io](https://link.zhihu.com/?target=http%3A//github.io) |
| 用于保存的目标分支 | main |
| 目标文件的路径 (例如，/wiki/) | / |
| 目标文件的文件名称 (例如，index.html) | index.html |

现在，你就配置好你独享的个人笔记本tiddlywiki啦！

继续打造，就需要添加一些插件了，添加的方式也很简单，找到插件，直接拖进来就OK了。

enjoy it！