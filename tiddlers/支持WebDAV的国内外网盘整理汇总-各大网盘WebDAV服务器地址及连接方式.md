> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [wzfou.com](https://wzfou.com/webdav-wangpan/)

> WebDAV 虽然用处非常大，但是国内的网盘服务鲜有支持 WebDAV 协议的，就目前来说也就只有坚果云网盘可以使用 WebDAV，而国外的 WebDAV 网盘则比较多，例如我们常用的 Dropbox、Box 等网盘就......

WebDAV 是一组基于超文本传输协议的技术集合，有利于用户间协同编辑和管理存储在万维网服务器文档。很多的软件例如 WPS、[Joplin](https://wzfou.com/joplin/)、Keepass 等都可以结合 WebDAV 实现数据云存储，让你不用依赖于服务商的云存储服务，不仅保护隐私，还可以自定义各种功能。

不过，WebDAV 虽然用处非常大，但是国内的网盘服务鲜有支持 WebDAV 协议的，就目前来说也就只有[坚果云](https://wzfou.com/tag/jianguoyun/)网盘可以使用 WebDAV，而国外的 WebDAV 网盘则比较多，例如我们常用的 [Dropbox](https://wzfou.com/tag/dropbox/)、[Box](https://wzfou.com/tag/box/) 等网盘就可以使用 WebDAV，当然速度肯定不如坚果云了。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_00-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_00.png)

本篇文章就来分享一下国内外支持 WebDAV 网盘服务，如果这些网盘没有你适用的，你也可以尝试自建网盘，像 [Nextcloud](https://wzfou.com/tag/nextcloud/)、[Seafile](https://wzfou.com/tag/seafile/) 这类自建网盘都是支持 WebDAV 的。同时我们还可以使用 RaiDrive 来挂载支持 WebDAV 的网盘，方便你统一管理各大 WebDAV 网盘。

1.  [NextCloud 从入门到精通 - 自建网盘搭建个人云存储系统](https://wzfou.com/nextcloud-huizong/)
2.  [Seafile 免费同步云盘安装与使用 - 自建私有云盘 打造个人云存储系统](https://wzfou.com/seafile-yunpan/)
3.  [本地网络磁盘 RaiDrive 挂载 Dropbox,Google Drive,OneDrive 支持 WebDAV,FTP,SFTP](https://wzfou.com/raidrive/)

**PS：更新记录.**

> 1、NextCloud 与 Seafile 是两个非常优秀的网盘自建系统，有关的对比你可以查看：[NextCloud 与 Seafile 对比使用 - NextCloud 各项全能 Seafile 优势突出](https://wzfou.com/nextcloud-seafile/)。2021.4.21

一、WebDAV 网盘汇总
-------------

<table data-wptb-adaptive-table="0" data-wptb-cells-width-auto-count="1" data-wptb-table-tds-sum-max-width="403" data-table-columns="3" data-reconstraction="1" data-wptb-extra-styles="LyogRW50ZXIgeW91ciBjdXN0b20gQ1NTIHJ1bGVzIGhlcmUgKi8=" role="table" data-wptb-horizontal-scroll-status="1" data-wptb-responsive-directives="eyJyZXNwb25zaXZlRW5hYmxlZCI6dHJ1ZSwicmVzcG9uc2l2ZU1vZGUiOiJhdXRvIiwicHJlc2VydmVSb3dDb2xvciI6ZmFsc2UsInJlbGF0aXZlV2lkdGgiOiJ3aW5kb3ciLCJoZWFkZXJGdWxseU1lcmdlZCI6ZmFsc2UsIm1vZGVPcHRpb25zIjp7ImF1dG8iOnsiZGlzYWJsZWQiOnsiZGVza3RvcCI6ZmFsc2UsInRhYmxldCI6ZmFsc2UsIm1vYmlsZSI6ZmFsc2V9LCJ0b3BSb3dBc0hlYWRlciI6eyJkZXNrdG9wIjpmYWxzZSwidGFibGV0Ijp0cnVlLCJtb2JpbGUiOnRydWV9LCJyZXBlYXRNZXJnZWRIZWFkZXIiOnsiZGVza3RvcCI6dHJ1ZSwidGFibGV0Ijp0cnVlLCJtb2JpbGUiOnRydWV9LCJzdGF0aWNUb3BSb3ciOnsiZGVza3RvcCI6ZmFsc2UsInRhYmxldCI6ZmFsc2UsIm1vYmlsZSI6ZmFsc2V9LCJjZWxsU3RhY2tEaXJlY3Rpb24iOnsiZGVza3RvcCI6InJvdyIsInRhYmxldCI6InJvdyIsIm1vYmlsZSI6InJvdyJ9LCJjZWxsc1BlclJvdyI6eyJkZXNrdG9wIjoxLCJ0YWJsZXQiOjEsIm1vYmlsZSI6MX19fSwiYnJlYWtwb2ludHMiOnsiZGVza3RvcCI6eyJuYW1lIjoiZGVza3RvcCIsIndpZHRoIjoxMDI0fSwidGFibGV0Ijp7Im5hbWUiOiJ0YWJsZXQiLCJ3aWR0aCI6NzAwfSwibW9iaWxlIjp7Im5hbWUiOiJtb2JpbGUiLCJ3aWR0aCI6MzAwfX19" data-wptb-apply-table-container-max-width="1" data-wptb-table-container-max-width="690" data-wptb-td-width-auto="102" data-wptb-sortable-table-vertical="1" data-wptb-breakpoint="desktop"><tbody><tr><td tabindex="0" aria-controls="tablepress-52-no-20" rowspan="1" colspan="1" aria-label="名称: 以升序排列此列" data-x-index="0" data-y-index="0" data-sorted-vertical="ask"><p>名称</p></td><td tabindex="0" aria-controls="tablepress-52-no-20" rowspan="1" colspan="1" aria-label="免费容量: 以升序排列此列" data-x-index="1" data-y-index="0" data-sorted-vertical="ask"><p>免费容量</p></td><td tabindex="0" aria-controls="tablepress-52-no-20" rowspan="1" colspan="1" aria-label="WebDAV地址: 以升序排列此列" data-x-index="2" data-y-index="0" data-wptb-css-td-auto-width="true" data-sorted-vertical="ask"><p>WebDAV 地址</p></td></tr><tr><td data-x-index="0" data-y-index="1"><p>坚果云</p></td><td data-x-index="1" data-y-index="1"><p>1GB</p></td><td data-x-index="2" data-y-index="1" data-wptb-css-td-auto-width="true"><p>https://dav.jianguoyun.com/dav/</p></td></tr><tr><td data-x-index="0" data-y-index="2"><p>Dropbox</p></td><td data-x-index="1" data-y-index="2"><p>2GB</p></td><td data-x-index="2" data-y-index="2" data-wptb-css-td-auto-width="true"><p>https://dav.dropdav.com/</p></td></tr><tr><td data-x-index="0" data-y-index="3"><p>box</p></td><td data-x-index="1" data-y-index="3"><p>10GB</p></td><td data-x-index="2" data-y-index="3" data-wptb-css-td-auto-width="true"><p>https://dav.box.com/dav</p></td></tr><tr><td data-x-index="0" data-y-index="4"><p>TeraCloud</p></td><td data-x-index="1" data-y-index="4"><p>15GB</p></td><td data-x-index="2" data-y-index="4" data-wptb-css-td-auto-width="true"><p>https://nanao.teracloud.jp/dav/</p></td></tr><tr><td data-x-index="0" data-y-index="5"><p>4Shared</p></td><td data-x-index="1" data-y-index="5"><p>15GB</p></td><td data-x-index="2" data-y-index="5" data-wptb-css-td-auto-width="true"><p>https://webdav.4shared.com</p></td></tr><tr><td data-x-index="0" data-y-index="6"><p>PowerFolder</p></td><td data-x-index="1" data-y-index="6"><p>5GB</p></td><td data-x-index="2" data-y-index="6" data-wptb-css-td-auto-width="true"><p>https://my.powerfolder.com/webdav</p></td></tr><tr><td data-x-index="0" data-y-index="7"><p>CloudMe</p></td><td data-x-index="1" data-y-index="7"><p>付费</p></td><td data-x-index="2" data-y-index="7" data-wptb-css-td-auto-width="true"><p>https://webdav.cloudme.com/XXXXXX</p></td></tr><tr><td data-x-index="0" data-y-index="8"><p>iDriveSync</p></td><td data-x-index="1" data-y-index="8"><p>5GB</p></td><td data-x-index="2" data-y-index="8" data-wptb-css-td-auto-width="true"><p>https://dav.idrivesync.com/zotero</p></td></tr><tr><td data-x-index="0" data-y-index="9"><p>Yandex Disk</p></td><td data-x-index="1" data-y-index="9"><p>10GB</p></td><td data-x-index="2" data-y-index="9" data-wptb-css-td-auto-width="true"><p>https://webdav.yandex.ru</p></td></tr><tr><td data-x-index="0" data-y-index="10"><p>Koofr</p></td><td data-x-index="1" data-y-index="10"><p>2GB</p></td><td data-x-index="2" data-y-index="10" data-wptb-css-td-auto-width="true"><p>https://app.koofr.net/dav/Koofr</p></td></tr><tr><td data-x-index="0" data-y-index="11"><p>MyDrive</p></td><td data-x-index="1" data-y-index="11"><p>100M</p></td><td data-x-index="2" data-y-index="11" data-wptb-css-td-auto-width="true"><p>https://webdav.mydrive.ch</p></td></tr><tr><td data-x-index="0" data-y-index="12"><p>Memopal</p></td><td data-x-index="1" data-y-index="12"><p>3GB</p></td><td data-x-index="2" data-y-index="12" data-wptb-css-td-auto-width="true"><p>https://dav.memopal.com/</p></td></tr><tr><td data-x-index="0" data-y-index="13"><p>Storage Made Easy</p></td><td data-x-index="1" data-y-index="13"><p>5GB</p></td><td data-x-index="2" data-y-index="13" data-wptb-css-td-auto-width="true"><p>https://webdav.storagemadeeasy.com</p></td></tr><tr><td data-x-index="0" data-y-index="14"><p>FileAnywhere</p></td><td data-x-index="1" data-y-index="14"><p>付费</p></td><td data-x-index="2" data-y-index="14" data-wptb-css-td-auto-width="true"><p>https://webfolder.filesanywhere.com</p></td></tr><tr><td data-x-index="0" data-y-index="15"><p>iCloud</p></td><td data-x-index="1" data-y-index="15"><p>5GB</p></td><td data-x-index="2" data-y-index="15" data-wptb-css-td-auto-width="true"><p>http://icloud.com/en/webdav</p></td></tr><tr><td data-x-index="0" data-y-index="16"><p>城通网盘</p></td><td data-x-index="1" data-y-index="16"><p>500G</p></td><td data-x-index="2" data-y-index="16" data-wptb-css-td-auto-width="true"><p>https://www.ctfile.com/</p></td></tr></tbody></table>

二、坚果云
-----

网站：

1.  https://www.jianguoyun.com/

免费版上传流量 1G / 月，下载流量 3G / 月，空间受限于上传流量（每月拥有 1GB 上传流量，至多可上传 1GB 文件。）当前 WebDAV 客户端和网页端上传大小的限制是一致的，默认为 500M。免费版用户限制访问频率为每 30 分钟不超过 600 次请求。付费用户限制访问频率为每 30 分钟不超过 1500 次请求。

> 坚果云的服务器地址：https://dav.jianguoyun.com/dav/
> 
> 用户名是坚果云账号，
> 
> 密码是一开始设置的应用密码（非坚果云账号登录密码）

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_01-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_01.png)

目前坚果云的 WebDAV 协议单次请求文件数（包含文件和文件夹）为 750 个，支持分多页多次加载。如果您使用 WebDAV 的三方工具未实现按分页多次加载，可能会出现文件同步不完整的情况，建议您使用坚果云客户端进行直接同步。

三、Dropbox
---------

网站：

1.  https://www.dropbox.com/

Dropbox 免费 2GB，可以邀请好友扩容 16GB 。

> WebDAV 网址：https://dav.dropdav.com/
> 
> 账号：你的 Dropbox 账号
> 
> 密码：你的 Dropbox 密码

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_02-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_02.png)

四、box
-----

1.  https://www.box.com/

Box 免费空间容量为 10GB，单个文件大小限制为 250MB。**2022.8.23 更新：**有朋友反馈说目前 Box 已经不再支持 WebDAV。

> WebDAV 网址: https://dav.box.com/dav  
> 账号密码: Your Box login email address and password.  
> Note: Web browser access is not supported. You must use a WebDAV client.

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_03-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_03.png)

五、TeraCloud
-----------

网站：

1.  https://teracloud.jp/en/

TeraCloud 是日本老牌网盘，免费空间为 10GB，另外一个通过邀请可以获得 5GB 额外空间。

> WebDAV 在线浏览器：  
> https://nanao.teracloud.jp/browser/  
> WebDAV 地址：  
> https://nanao.teracloud.jp/dav/
> 
> 账号密码：你的 TeraCloud 账号密码

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_04-1-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_04-1.png)

六、4Shared
---------

网站：

1.  https://m.4shared.com/

4shared 是一家文件托管服务公司，公司由 Alex Lunkov 和 Sergey Chudnovsky 于 2005 年在 成立，免费用户为 15GB，单个文件大小为 2GB。

> WebDAV 地址：https://webdav.4shared.com/
> 
> 账号密码：Enter your 4shared account login and password;

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_05-1-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_05-1.png)

七、PowerFolder
-------------

网站：

1.  https://www.powerfolder.com/

PowerFolder 是国外一个同步工具，支持 Windows、Mac、Linux 等多平台，免费用户提供 5GB 的容量。 PowerFolder 的 WebDAV URL 如下:

> Login at http://my.powerfolder.com or at your organization’s PowerFolder cloud URL.
> 
> Click on a folder to get the WebDAV URL for.
> 
> Click on **Settings**.
> 
> Copy the **WebDAV URL**.

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_06-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_06.png)

八、iDriveSync
------------

网站：

1.  https://www.idrivesync.com/

DriveSync 网盘工具是一个免费类 Dropbox 同步备份工具，支持 windows、mac、iOS、Android 多平台。 IDriveSync 免费用户提供 5GB 容量。

> WebDAV server ：https://dav.idrivesync.com
> 
> 账号密码： your IDriveSync username and password.

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_08-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_08.png)

九、Yandex Disk
-------------

网站：

1.  https://disk.yandex.com/

Yandex Disk 是俄罗斯一家非常有名的网盘服务，免费用户提供 10GB 容量。

> WebDAV：https://webdav.yandex.com
> 
> 账号密码：你的 Yandex Disk 账号密码。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_09-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_09.png)

十、Koofr
-------

网站：

1.  https://koofr.eu/

Koofr 是一家来自欧洲的网盘服务商，免费用户提供 2GB 存储容量，Koofr 网盘最大的优势是可以在线管理你的 [Dropbox](https://wzfou.com/tag/dropbox/)、[Onedrive](https://wzfou.com/tag/onedrive/)、[Google Drive](https://wzfou.com/tag/google-drive/) 文件，并且支持 WebDAV，

> The WebDAV connection settings:
> 
> Host: _https://app.koofr.net/dav/Koofr_
> 
> Port: _443_
> 
> User: _the email address that you used when creating a Koofr account_
> 
> Password: _the password that you generated through the Koofr webapp_
> 
> **Note**: If there is a Root or Path field available in the WebDAV settings of the service you are trying to connect, you must input _https://app.koofr.net_ into the Host field and _/dav/Koofr_ into the Root field.
> 
> **Note**: If you want to create a subfolder, include it into the Root field _/dav/Koofr/pathtosubfolder_.

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_10-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2021/01/webdav-wangpan_10.png)

十一、城通网盘
-------

网站：

1.  https://www.ctfile.com/

城通网盘是一个老牌的国产网盘，只有付费用户才能使用 WebDAV。

![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2023/02/ctdrivep-680x366.png)

文章出自：[挖站否](https://wzfou.com/) [https://wzfou.com/webdav-wangpan/](https://wzfou.com/webdav-wangpan/)，版权所有。本站文章除注明出处外，皆为作者原创文章，可自由引用，但请注明来源。