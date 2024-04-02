[TiddlyWiki的](https://static.baty.net/archived-websites/baty.blog-archive/topic/tiddlywiki/index.html) 10月 03， 2021 3分钟阅读

短版本：我正在使用[WebDAV服务器](https://www.schimera.com/products/webdav-nav-server/)将[我的TiddlyWiki wiki](https://rudimentarylathe.wiki/)作为独立的HTML文档进行管理，该服务器可通过[Tailscale](https://tailscale.com/)从任何地方安全访问，我现在可以将图像拖放到内容中，并自动上传和链接它们。太棒了！

尽管我很喜欢 TiddlyWiki，但我从来不喜欢用它管理图像。嵌入式图像是最简单的，但会迅速增加 wiki 的 HTML 文件大小，所以我引用了它们。我用了几种方法。

作弊版本是只使用我之前上传到 [Flickr](https://www.flickr.com/photos/jbaty/) 的图像的嵌入代码。第二个最佳选择是将图像放在与 wiki 本身相同的目录内的 /files 目录中，并使用类似 .`[img[files/my-image-file.png]]`

这并不_难_做到，但必须将每个图像移动到我的 wiki/files 目录，然后手写路径/文件名以创建链接会增加足够的摩擦，阻止我像其他方式一样自由地使用图像。

[TiddlyWiki 5.2.0](https://tiddlywiki.com/#Release%205.2.0) 最近发布了，它包含一个很棒的新功能，让我可以将图像拖放到一个打开的“tiddler”中，然后自动嵌入和链接。这是一个了不起的改进，但它仍然将图像嵌入到 wiki 文件中，我希望避免这种情况。

输入 [Saq Imtiaz](https://twitter.com/saqimtiaz) 的 [File Uploads 插件](https://saqimtiaz.github.io/tw5-file-uploads/)，然后为 WebDAV 提供全新的 PUT 选项。

这对我来说都是很新的，所以我可能没有资格写一个完整的教程，但这就是我所做的......

将我的wiki升级到5.2.0。（[https://tiddlywiki.com/upgrade.html](https://tiddlywiki.com/upgrade.html))

通过简单的拖放到我的 wiki 文件中安装了 [File Uploads 插件](https://saqimtiaz.github.io/tw5-file-uploads/)和随附的 PUT 插件（TiddlyWiki 很酷）。

通过告诉它使用“PUT”上传器以及我希望上传去哪里（相对于 wiki 文件本身）来配置插件。我选择了“files/2021”。

![](https://static.baty.net/archived-websites/baty.blog-archive/content/images/2021/10/CleanShot-2021-10-03-at-16.05.29.png)

配置文件上传插件

我使用[适用于 macOS 的 WebDAVNav Server 应用程序](https://www.schimera.com/products/webdav-nav-server/)通过 WebDAV 运行我的 wiki。其他操作系统还有其他选项，但我不熟悉这些。对我来说，好处是我可以用任何浏览器打开和保存我的wiki，不需要其他扩展。我在 Mac Mini 上运行 WebDAV 服务器，并通过 https://localhost:8080/index.html 访问它。

这就是奇迹发生的地方。我打开一个 tiddler，将图像拖入其中，然后砰！文件将上传到files/2021文件夹，并自动插入wiki文本链接。太酷了。

在运行 WebDAV 服务器的 Mac Mini 上编辑 wiki 时，这都是花花公子，但是在我的 MacBook Air 上呢？我可能会弄清楚 LAN 上 Mini 使用的 IP 并以这种方式访问它，但这只有在我想进入动态 DNS 和端口转发时才适用于我家。（我没有）。

输入 [Tailscale](https://tailscale.com/)，“零配置 VPN。在几分钟内安装到任何设备上，为您管理防火墙规则，并在任何地方工作。

在不到一个小时的时间里，我在所有 Mac、iPhone 和 iPad 上都启动并运行了 Tailscale。Tailscale 提供了一个可以从我所有设备访问的专用网络。这意味着我可以从任何地方通过 https://100.74.14.72:8080/index.html 访问和编辑我的wiki。（该 IP 不可公开路由，因此可以安全地共享它。

它也适用于 WebDAV PUT 上传。我可以将图像从 iPad 上的“照片”应用程序拖到 Safari 中，然后文件最终会在我的 Mac Mini 上找到它所属的位置。魔法！

我还不知道这种方法的陷阱是什么，但到目前为止，它已经解决了我管理包含我所有设备图像的单文件 wiki 的所有问题。

我的 wiki 是通过 Github Pages 发布的，所以为了推送更新，我确实需要提交并推送 reppo。我使用 SyncThing 同步了 repo 目录，因此更改在我的两台 Mac 上始终可用。虽然我可以从 iOS 编辑我的本地版本的 wiki，但我还不能从那里发布它。

它可能看起来像很多大惊小怪和活动部件，但到目前为止，我还没有感到任何痛苦。所有单独的部分（TiddlyWiki、WebDAV 服务器、Tailscale、SyncThing 等）都可以毫无问题地运行，并且它们之间没有太多的依赖关系。

我希望这有足够的意义来帮助您入门。请随时要求我澄清您认为令人困惑或遗漏的任何内容。