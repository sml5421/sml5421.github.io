很多人说不懂技术，配置 TiddlyWiki 和处理保存/免费同步/免费发布博客比较麻烦，所以我在字节时用晚上的业余时间开发了一个零配置的 TiddlyWiki 桌面版 APP [tiddly-gittly/TiddlyGit-Desktop](https://link.zhihu.com/?target=https%3A//github.com/tiddly-gittly/TiddlyGit-Desktop) 欢迎 star。下载地址 [releases/latest （需要翻墙）](https://link.zhihu.com/?target=https%3A//github.com/tiddly-gittly/TidGi-Desktop/releases/latest)，也可以加下面的QQ群在群文件里下载。

用这个App一键打开，即可使用强大美观好用的 TiddlyWiki。

* * *

TiddlyWiki可以替代Notion和EverNote作为个人知识管理系统吗？

我的 Wiki：[onetwo.ren/wiki](https://link.zhihu.com/?target=https%3A//onetwo.ren/wiki/) （ [Vercel 国内加速访问](https://link.zhihu.com/?target=https%3A//onetwo-wiki.vercel.app/) ）

太微中文教程：[https://tw-cn.netlify.app/](https://link.zhihu.com/?target=https%3A//tw-cn.netlify.app/) （ [只读版访问地址 Vercel 加速版（高速访问）](https://link.zhihu.com/?target=https%3A//tiddly-wiki-chinese-tutorial.vercel.app/)）

有疑问可以加入 TiddlyWiki 爱好者 QQ 群 946052860 ，或点击链接加入QQ频道【太微TiddlyWikI】：[https://qun.qq.com/qqweb/qunpro/share?\_wv=3&\_wwv=128&inviteCode=JBRKi&businessType=9&from=246610&biz=ka](https://link.zhihu.com/?target=https%3A//qun.qq.com/qqweb/qunpro/share%3F_wv%3D3%26_wwv%3D128%26inviteCode%3DJBRKi%26businessType%3D9%26from%3D246610%26biz%3Dka) ，或用 Bing 搜索微信群集智俱乐部注意力与知识管理群加入我所在的知识管理社区一起讨论。

视频版：[林一二：入门太微（TiddlyWiki）构建你的数字化第二大脑_哔哩哔哩_bilibili](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV1Kq4y1y7GN)

* * *

我曾经用过很多年的印象笔记，里面装着四处收集来的碎片内容，比如[什么是「共产中文腔调」？ \- 调查类问题 \- 知乎](http://www.zhihu.com/question/19687065)、我高考的分数截图等等；我也用了几年的 Notion，用它记待办事项、给认识的人写备忘小传；我还用了很久的 Anki，用它把英语单词、数学公式、算法套路等碎片知识装进脑中；我也了解过 Roam Research，它可以通过双向链接增加笔记的可发现性。

但这些工具似乎都不关注两个对我来说很关键的概念：「元信息」和「自动化」。我认为，只有能充分保存元信息的自动化的知识管理系统才能称得上「好用」。

这么说来，个人知识管理系统似乎有一个不可能三角：**免费-好用-好看，只能拥有其中两样**。Notion 要付费、印象笔记不好用、Quip 和飞书等系统不是为个人服务的……

然而 [TiddlyWiki](https://link.zhihu.com/?target=https%3A//tiddlywiki.com/) （太微）似乎打破了这个不可能三角，引入了第四个元素：它 **免费、好用，还蛮好看** ，唯一的缺点就是需要具备动手能力才能把积木式的它拼成自己想要的形状。对于有动手能力的人来说，它就是完美的。

![](https://pic3.zhimg.com/v2-1802bc7d7dee82965ef62f497bad5eca_b.jpg)
![](https://pic3.zhimg.com/v2-c442414d152e9710fca4d26bdcfa14f6_b.jpg)

首先我来简单谈谈我心中 TiddlyWiki 的美观、免费和强大之处。

美观的 TiddlyWiki（太微）
------------------

我之前喜欢 Notion 的一个重要理由就是它的设计很好看，所以我配置自己的 wiki 时，就打开 notion 网页版，用开发者工具复制它的样式表，择其善者而从之。

### 添加自定义样式

给一个 Tiddler 加上 $:/tags/Stylesheet 标签即可让它在 wiki 启动时加到 wiki 的样式表里，例如我就在[自定义链接样式](https://link.zhihu.com/?target=https%3A//onetwo.ren/wiki%23%25E8%2587%25AA%25E5%25AE%259A%25E4%25B9%2589%25E9%2593%25BE%25E6%258E%25A5%25E6%25A0%25B7%25E5%25BC%258F)里黏贴适配了 Notion 的链接的样式，鼠标悬浮后会低调地变色，凸显一种简约的尊贵。

我还通过添加 backdrop-filter 给各种地方加上了毛玻璃效果。等未来不流行毛玻璃效果了，我自己再把它重新设计为最流行的样子。

免费的太微
-----

往 TiddlyWiki 里拖很多图片之后，通过 now.sh 发布的博客可能会越变越大。所以我通过[把图片文件的链接改成指向 Github 上的图片](https://link.zhihu.com/?target=https%3A//onetwo.ren/wiki%23%25E5%25A4%2596%25E7%25BD%25AE%25E6%2596%2587%25E4%25BB%25B6)，来减小生成的 HTML 的体积。

这相当于把 Github 作为免费无限容量的图床来使用了，只要浏览量不是特别大，就不会收到封禁邮件。

### 数据自有

在打开我的 Wiki 后，你可以随意编辑它，这只会改动浏览器里的缓存的 wiki 内容，不会影响我电脑上本地的内容、也不会影响我 Github 上的备份。

在浏览器里的缓存变化之后， TiddlyWiki 是怎么把内容持久化到别的地方的呢？就是靠 Saver（粗粒度保存器）和 SyncAdaptor（细粒度同步器）了。

官方有一个 GitHubSaver 插件，在填入 Github Token 之后可以在移动端、桌面 Web 端直接把修改后的 Wiki 保存到 Github 上，变成一个 HTML 文件备份。 而在桌面端启动 NodeJS 版 wiki 之后，则是一个 TiddlyWebSyncAdaptor 在把修改的 Tiddler 同步到文件系统上备份。

在未来，我们可以用 [solid-tiddlywiki-syncadaptor (WIP)](https://link.zhihu.com/?target=https%3A//github.com/linonetwo/solid-tiddlywiki-syncadaptor) 等自定义的同步器，把数据保存到任何我们想保存的地方，不受制于大公司，也不需要像用印象笔记一样购买会员服务。数据怎么保存、存在哪里都可以我们自己自由定制。

强大的太微
-----

我关注一个信息是什么，它从哪里来，要到哪里去……也就是关于信息的信息：标签、源谱、关联。我们的大脑会保存和一个信息相关的很多其他信息，而如果一个知识管理系统也同样保存了这些元信息，就可以用很贴近我们大脑的形式存储知识，让我们查找、利用知识都更加便捷。

自动化则能减少很多复制黏贴文本的劳作，还能让信息被以各种方式聚合，出现在更多地方，更容易被找到。

### 非线性写作

在我构思一篇文章时，我的思绪经常在记忆的网上游走，把很多与主题相关的碎片拼到脑中的文章里。但是，大脑和知识管理系统是不同步的，很多碎片内容并不存在于机器里，而只存在于大脑中。这时候要是先把碎片内容录入到电脑里，再回过头继续在记忆中漫游，就有可能打断漫游的思路，消弭刚刚产生的灵感。

更好的方法是，先用一个链接占坑：

```text
<<reuse-tiddler "允许用git-sync脚本自动同步代码">>
```

![](https://pic1.zhimg.com/v2-5ac2c06e78eb0e1191fa094abad4c804_b.jpg)

等整篇文章的框架写好之后，再回过头来点击「允许用 git-sync 脚本自动同步代码」的按钮，创建这篇碎片笔记，把具体内容录入其中，然后 TiddlyWiki 会自动把碎片内容填充到刚刚占的坑里。

### 重构：改善既有文档的设计

内容碎片化的好处有很多：

1.  可能会有多篇笔记要引用同样的内容，把这部分内容重构（refactor）出来，然后用 [Transclusion（嵌入）](https://link.zhihu.com/?target=https%3A//tiddlywiki.com/%23Transclusion)的方式把它们自动填充到多个坑里，而不是通过复制黏贴的方式填坑。这样以后如果要修改的话，改一处地方即可，不用找所有地方改，不会发生漏改的情况。
2.  可以添加段落级元信息，例如可以把一篇主题 A 的文章中的一个段落放到主题 B 的文件夹里，因为这个段落在谈主题 B。这样以后写主题 B 的文章时就很容易找到这个碎片作为参考资料。
3.  通过全文检索搜参考资料时，不用读大段的内容，可以直接看小段的参考资料是否对当下的自己有价值

既然内容碎片化好处这么大，我们肯定希望在把其他地方的内容复制黏贴到 TiddlyWiki 里的时候，就把它拆分得细一点。

这种简单的重构可以使用[文本切分插件](https://link.zhihu.com/?target=https%3A//tiddlywiki.com/editions/text-slicer/)来自动切分，也可以手动臻选出以后可能自己会用到的部分，加上合适的标签（相当于放到与标签同名的文件夹里）。

### 写 JS 用户脚本自动化操作

我已经习惯了用方便的 [Copy On Select Firefox 插件](https://link.zhihu.com/?target=https%3A//addons.mozilla.org/zh-CN/firefox/addon/autocopy-we/)，现在到了 TiddlyWiki 桌面 App 里，我经常还是以为选中了就复制了，然后黏贴到别的地方才发现其实并没有复制，很不习惯。

这个功能 TiddlyWiki 显然不会自带，目前也没有搜到插件可以做这件事。所以我自己重新写了一个[适配 TiddlyWiki 的小脚本](https://link.zhihu.com/?target=https%3A//onetwo.ren/wiki/%23%2524%253A%252Fplugins%252Flinonetwo%252Fcopy-on-select) （后来还是打包成插件了，所以现在这个是插件的链接），做成了启动脚本。脚本比插件要轻量，不需要打包发布等等繁琐的流程，自己想要啥功能半小时写完调试好就能用。

通过把 JS 代码加上 $:/tags/RawMarkup Tag 、并用 <script type="text/javascript"> </script> 包裹，就可以让这段代码在 wiki 启动时执行了。

我在代码里就获取选区，判断当前是不是在编辑器里，如果不是就复制。

这也是太微最强大的地方，所有插件、脚本、功能，本质上都是笔记，和其他笔记一样都可以在太微里编辑。写完之后，配置好笔记的类型为 JS 脚本，刷新页面就能生效。

所以理论上可以在一个笔记里跑一个迷你版的太微，是不是很有元编程和 Quine（奎恩）的感觉？

### 覆盖系统默认行为

TiddlyWiki 里几乎所有功能都是可覆盖的，一般分为三种：

1.  wikitext ，主要用于写 UI，例如卡片的渲染模板，修改后可以做到「在每个卡片底下显示相关卡片」、「反向链接」等功能
2.  filter ，可以和 wikitext 结合起来写渲染模板，也可以用于「[把加了 APrivateContent 标签的笔记保存到私有仓库里面](https://link.zhihu.com/?target=https%3A//onetwo.ren/wiki%23%2524%253A%252Fconfig%252FFileSystemPaths)」等功能
3.  JS，所有 wikitext 和 filter 最终都要依赖 JS 的实现，覆盖想要修改的 JS 可以实现「[鼠标悬浮预览插件本来不会自动关上预览窗口，我让它自动关闭](https://link.zhihu.com/?target=https%3A//onetwo.ren/wiki%23%25E9%25BC%25A0%25E6%25A0%2587%25E6%2582%25AC%25E6%25B5%25AE%25E9%25A2%2584%25E8%25A7%2588%25E5%2586%2585%25E9%2583%25A8%25E9%2593%25BE%25E6%258E%25A5)」等功能

TiddlyWiki 和 Anki 很相似的一点是，笔记和卡片是分离的，也就是笔记只保留内容和元信息，在 Wiki 实际运行时，才通过模板渲染为卡片。所以可以通过写 wikitext 宏或 JS 宏，来在运行时对展示做各种变换。

### 聚合数据及推理

[Datalog 及其方言](https://link.zhihu.com/?target=https%3A//github.com/tonsky/datascript) 是用于输入知识还有聚合、推理、利用知识的编程语言，虽然很强大，但使用起来还是有一定门槛的。

TiddlyWiki 让我们可以用更容易学会的方式，在美观的界面里为碎片知识加上元信息，例如可以给一个「我的剪刀」的笔记，加上 location: 客厅 的元信息，相当于描述了知识「我的剪刀放在客厅里」。这样就可以写一个简单的 filter 来把所有放在客厅里的物品列成一个列表，展示在一个动态生成的笔记里了。

在以后你找不到剪刀的时候，就可以直接搜索「我的剪刀」，然后查看它的 location 字段知道它放在哪里。更可以把这些元信息传给一个问答机器人，你语音问他你的剪刀在哪，它通过简单的意图理解、检索、推理、取字段就能帮你找到客厅里的剪刀了。

### 图遍历

完善的知识体系常常是一个网状的结构，我通过[鼠标悬浮链接显示相关内容](https://link.zhihu.com/?target=https%3A//onetwo.ren/wiki%23%25E9%25BC%25A0%25E6%25A0%2587%25E6%2582%25AC%25E6%25B5%25AE%25E9%25A2%2584%25E8%25A7%2588%25E5%2586%2585%25E9%2583%25A8%25E9%2593%25BE%25E6%258E%25A5)这个插件（当然，经过了我自己的修改），可以展示每个笔记所在的文件夹（[文件夹即标签](https://link.zhihu.com/?target=https%3A//onetwo.ren/wiki%23%25E5%259C%25A8%2520TiddlyWiki%2520%25E4%25B8%25AD%25E4%25BD%25BF%25E7%2594%25A8%25E8%2599%259A%25E6%258B%259F%25E6%2596%2587%25E4%25BB%25B6%25E5%25A4%25B9)）、反向链接（链入的内容，类似 [RoamResearch](https://link.zhihu.com/?target=https%3A//nesslabs.com/roam-research-alternatives)）、笔记作为一个文件夹装了什么内容（更确切地说，笔记相当于文件夹的 Readme）。

![](https://pic1.zhimg.com/v2-1530b75775bf52c6fab5cbea003af8d8_b.jpg)

介绍太微的使用方式
---------

TiddlyWiki 是一个自由免费的软件，自然也就缺乏财力和精力将它包装得更加易用。

一直以来都需要用户有一定的技术和折腾劲来配置它。不得不说过程还是稍显繁琐的，对于曾经分别使用过其中每一项技术的我来说，从零搭建环是没有特别大的阻碍的，但是对于非程序员来说，可能就有点吃不消了。

所以我将我的配置经验写成了开源代码，使太微变成了一个漂亮的桌面应用，能享受免费的无限大的存储、管理私有数据、发布㐓公开的知识到博客里。在最后我会分别介绍 TiddlyWiki 具体美观好用免费在哪里。

这个应用结合了 TiddlyWiki 和 Git 的功能，所以称为 TiddlyGit（太记）。

### 下载太记（TiddlyGit）

下载地址在 [Release · tiddly-gittly/TiddlyGit-Desktop](https://link.zhihu.com/?target=https%3A//github.com/tiddly-gittly/TiddlyGit-Desktop/releases/latest) ，不过也可以按文章开头写的联系方式找到群来下载。

在下载页的最底下可以看到全平台的下载链接，其中 arm64 指的是 M1 芯片等电脑用的，x64 是通常的电脑用的。Windows 一般下载 Windows-x64-setup.exe 就好。macOS 用户下载 darwin .zip 的 。

![](https://pic4.zhimg.com/v2-dcab1e82bace8b73cec2cffde39aa017_b.jpg)

macOS 用户解压完记得拖进「应用程序」目录里，不然可能打不开。而且记得参考 [macOS无法验证此App不包含恶意软件，怎么解决？](https://www.zhihu.com/question/412633194/answer/2049455275)

### 使用太记（TiddlyGit）

打开应用后我们跟着箭头点击添加按钮，创建第一个Wiki：

![](https://pic1.zhimg.com/v2-7ebe0a5cca52c9a2030b7ec0bb74c3d4_b.jpg)

弹出来的界面里默认是创建新Wiki，默认是创建本地知识库。下面表单里的每个选项和按钮都加了中英文多语言的注释，大部分默认即可。

![](https://pic3.zhimg.com/v2-5544b44a1fc0c8fefed8ef8dad6f5bea_b.jpg)

如果你拥有 [Github](https://link.zhihu.com/?target=https%3A//github.com/) 账号，就可以点一下蓝色的切换开关，切换成创建在线知识库，通过Github账号同步备份到云端，这样一个配置好的 Wiki 仓库就会出现在你的 Github 账号下了。

没有账号或者网络不佳的用户，用本地的Wiki也行，自己用网盘手动同步文件夹也可以做备份。

### 填知识库文件夹所在的位置

*   在表单里选择好知识库文件夹所在的位置
*   填好 Wiki 名字等信息（例如默认是「wiki」，也可以用中文例如「我的知识库」）
*   然后点击红色的「创建Wiki」按钮
*   Wiki就会生成文件夹，并启动了。

### 使用太记

新建的 Wiki 还是空的，我们可以点右边的加号➕，来新建笔记（在太微里称作 Tiddler 小太，Tiddler 英文是「很小段的笔记」的意思）

或者点 MD↓ 按钮来创建 Markdown 笔记。

第一篇笔记可以改个标题叫「Index」：

![](https://pic3.zhimg.com/v2-be1b10d3e0bc519bc3d245fbfb4fca8a_b.jpg)

点左边的眼睫毛图标可以打开预览，点中间的对勾✔️可以保存。

保存之后我们把这个地方的「默认开启的条目」的内容改成「Index」。

![](https://pic2.zhimg.com/v2-7a00bba1b094462b7ef7a55b7eed6499_b.jpg)

之后就可以在应用启动时自动打开我们的 Index 笔记了，也可以在右边的文件目录里直接点开 Index ，或者点左边的工作区图标也可以打开 Index ：

![](https://pic4.zhimg.com/v2-a9a3fee0ba893b3961dfccf7a0daa4ab_b.jpg)

我们点击 Index 笔记的中间的这个标签图标，可以创建一个加了「Index」标签的新笔记。

保存新笔记（上图中新笔记的标题是「新条目」）之后，它会出现在右边的「文件目录」里，形成笔记树状（其实是有向图）结构，可以当文件夹功能来用。详细说明见红圈里的「使用帮助」这个笔记链接。

之后就是不停添加新笔记了，文本框上方有各种功能，例如文本片段功能↓ ，可以看其他太微的教程来学习。

![](https://pic3.zhimg.com/v2-f9432308ae6fbf2de41052b10dd5938a_b.jpg)

一开始可以先从不断添加新笔记出发，等积攒的笔记需要用高级功能整理了，再去学习高级功能，一般来说想要啥功能都有相关插件，如果没有插件也可以请人或者自己用 JS 很快写出来，理论上不会碰到天花板。

### 从本地Wiki改为云端同步Wiki

第一次创建可以就建本地Wiki，之后想云同步了，就在 Github 上建一个空白的仓库，然后看这些按钮：

![](https://pic3.zhimg.com/v2-c46b84f5c6ad3e3f4a14f7d4fc5c3ec2_b.jpg)

点这个「↓Code」就可以看到仓库的 git 地址，我们接下来要把 ssh 形式的仓库地址配置到本地仓库里，这是为了避免[无法同步的问题](https://link.zhihu.com/?target=https%3A//github.com/simonthum/git-sync/issues/17)：

![](https://pic2.zhimg.com/v2-f319f2064a60cd6ae8d708df85d2220d_b.jpg)

可以先装一个 git 工具：[桌面应用 Github Desktop](https://link.zhihu.com/?target=https%3A//desktop.github.com/) ，安装好之后，用[桌面应用 Github Desktop](https://link.zhihu.com/?target=https%3A//desktop.github.com/) 打开本地的 Wiki 文件夹，过于简单就动脑子自行探索了。之后你在 Github Desktop 上就可以看到如下的界面：

![](https://pic2.zhimg.com/v2-c5a7155e090539a3a66349d288934bb1_b.jpg)

然后如图设置 git 仓库地址即可。

![](https://pic2.zhimg.com/v2-d81e5d27fcdb32fa0abfeea6a0a2fc91_b.jpg)
![](https://pic4.zhimg.com/v2-104fdc2d707959f80b974737fe7e82ef_b.jpg)

之后如果在太记的工作区设置里登录自己的Github账号，就可以享受自动同步了：

![](https://pic4.zhimg.com/v2-a19baf1d051b91fe67c3b80a1b2139f3_b.jpg)

也可以保持太记里的工作区设置为「本地知识库」，然后完全用 Github Desktop 来同步和提交，这样你甚至可以将内容备份到自己的私有自建 Git 服务上，做到完全的数据自有。

### 特色功能，变成快查小应用

打开设置界面，里面有一个 Attach to menu bar 的选项，勾上这个选项，可以作为快速搜索小工具使用。

![](https://pic1.zhimg.com/v2-08bb710029faa292891da008f516a5e4_b.jpg)

效果类似于这样：

![](https://pic3.zhimg.com/v2-c442414d152e9710fca4d26bdcfa14f6_b.jpg)

### 配置用户名

注意打开设置修改一下里面的用户名，从 `林一二`TiddlyGitUser 改成你自己的名字或网名。

![](https://pic2.zhimg.com/v2-7827b93f86d6ca94aa41de8854f88aa5_b.jpg)

### 私有内容

之前创建的代码仓库是公开的，所以同步备份上去的 wiki 就相当于你的博客，那如果我们希望添加自己的 TodoList 等等私有内容呢？

![](https://pic3.zhimg.com/v2-13c549d9e5ab17df9c60cb01a27eee82_b.jpg)

这时候就可以创建子知识库，我们以你给它取名为 `private-MyTiddlyWiki` 为例，首先把「即将新建的知识库文件夹名」改为 private-MyTiddlyWiki ，然后在标签名那边填一个用于标记私有笔记的标签名（例如「APrivateContent」或者「私有」）。

点击创建之后，太微会为你创建一个新的文件夹，之后如果你给一个 Tiddler 加上 APrivateContent 这个 tag ，TiddlyWiki 就会把你加到 Wiki 里的内容保存到刚刚创建的私有仓库里的 tiddlers 文件夹里了。

其具体原理是通过修改太记内的 $:/config/FileSystemPaths 来实现笔记的分发，将带标签的笔记分发到新建的私有文件夹里。Google 一下可以了解 FileSystemPaths 的更多技术细节，不过太记都将这些包装成了使用较为简单产品，不了解也没关系。

之后就可以将笔记同步到网上的私有仓库去了，或者选择只把主仓库同步到网上，私有文件夹则保留在本地离线使用等等。

### 配置开机启动和自动同步

都在设置里，翻翻就能看到了。

![](https://pic4.zhimg.com/v2-48db0903402bded4322e66f3b6515c9f_b.jpg)

### 部署公开内容为网站

既然我们有一些开放的内容，为什么不把它们发布成一个有自己域名的网站呢？这样你可以把你的一些笔记很方便地分享给朋友。

本模板中已经配置好了 Github Actions，当你备份 Wiki 到 Github 云端时，会自动把你的公开 wiki 中的内容发布为静态博客。访问地址类似 `linonetwo.github.io/wiki` ，将此处的 `linonetwo` 改成你的 Github 用户名，将 `wiki` 改成你的仓库名即可。

如果你已经提交过一次备份，那么就可以试着访问一下啦！

### 插件仓库

本模板中已经预置了几个插件仓库，点击右上角的「打开控制台」按钮打开 `ControlPanel` 后，就可以在「插件」标签页里点击「获取更多插件」看到它们了。

我也已经在太记里预置了一些开源插件，例如我写的 `copy-on-select` 提供了选中即复制的快捷功能、`inverse-link-and-folder` 提供了反向链接等等。

更多插件需要到 [TiddlyWiki Google Group](https://link.zhihu.com/?target=https%3A//groups.google.com/forum/%23%21forum/tiddlywiki) 里看最新动态来找，或者到QQ群里找人推荐。

结语
--

至此，一个有桌面端 App、能自动备份、能存储隐私信息、能发布内容为网站的，强大的知识管理系统就配置好啦！

TiddlyWiki 的[社区论坛](https://link.zhihu.com/?target=https%3A//groups.google.com/forum/%23%21forum/tiddlywiki)和 [Github 仓库](https://link.zhihu.com/?target=https%3A//github.com/Jermolene/TiddlyWiki5)非常活跃，每天都能看到新的点子涌现出来。大家出于对这个工具的喜爱，在不断贡献自己的想法和代码来推动 TiddlyWiki 变得越加美观、强大。在[集智俱乐部注意力与知识管理群](https://link.zhihu.com/?target=https%3A//swarma-km.hintsnet.com/%23%3A%25E5%2585%25B3%25E4%25BA%258E%25E6%259C%25AC%25E7%25AB%2599)里，大家也在积极讨论如何把 Notion、RoamResearch、TheBrain 的优点结合到 TiddlyWiki 里。

我也在做各种尝试，希望把 TiddlyWiki 和 Anki、语音助手、SoLiD POD 连接起来，让它作为一个数字化的我，承载我的各种知识，利用这些知识使我的生活变得更加便利。

如果你也为其美观、强大所动，欢迎也加入这个社区，搜索初用时疑问的解答、为其他新手解答疑惑，以及贡献自己的一技之长让更多人为其所动。