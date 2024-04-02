> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [wzfou.com](https://wzfou.com/alist/)

> AList 除了可以挂载网盘，还支持 FTP、SFTP、WebDAV、S3 等协议，利用 AList 你基本上可以将市面大部分云存储服务挂载成存储服务器了。

AList 是一个目录列表程序，支持挂载各大网盘以及云存储，目前支持的网盘有阿里云盘、OneDrive / Sharepoint、天翼云盘、GoogleDrive、蓝奏云、百度网盘、迅雷云盘、夸克网盘等。AList 提供了 Web 访问，你可以将各大网盘当作自己的存储服务器，随时随地在网络上下载查看。

AList 除了可以挂载网盘，还支持 FTP、SFTP、WebDAV、S3 等协议，利用 AList 你基本上可以将市面大部分云存储服务挂载成存储服务器了。同时，AList 还支持连接另一个 AList，也就是说你可以将两个已经安装了 AList 的服务器连接到一起，这样又可以扩充到全部存储服务器了。

AList 还有强大的文件预览功能，支持视频、音频、文档、PDF、图片预览等直接在线播放或者查看，甚至支持 ipa 安装，以及文本编辑器、README/HTML 渲染、文件永久链接等等。总之，AList 是一个比较理想的大批量文件共享和分享工具，安装简单，任何平台都可以使用。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_00-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_00.png)

这篇文章就来分享一下 [AList](https://wzfou.com/tag/alist/) 的安装与使用，更多的目录列表程序可以查看专题：[目录列表程序整理汇总](https://wzfou.com/mulu-lists/)。这里还有：

1.  [Resilio Sync 文件同步共享工具 - Resilio Sync Docker 安装与使用教程](https://wzfou.com/resilio-sync/)
2.  [S3 Browser 免费强大的 S3 存储管理软件 - 可管理兼容 S3 协议各类云存储](https://wzfou.com/s3browser/)
3.  [Linode 对象存储管理与使用教程 - 兼容 S3 协议的对象存储价格便宜超大存储](https://wzfou.com/linode-object-storage/)

一、AList 安装方法
------------

网站：

1.  官网：https://alist.nn.ci/zh/
2.  项目：https://github.com/alist-org/alist
3.  Docker：https://hub.docker.com/r/xhofe/alist
4.  文档：https://alist.nn.ci/zh/guide/
5.  演示：https://al.nn.ci/

### 1.1 准备 VPS 主机

[AList](https://wzfou.com/tag/alist/) 支持 Windows、Linux 等各大平台，如果想长期使用 AList，建议使用 VPS 来运行。现在的 VPS 主机基本上也是白菜价了，有关于 VPS 主机评测查看：[VPS 主机排行榜单](https://wzfou.com/vps-bangdan/)。

### 1.2 Docker 环境

（可选）有了 [VPS 主机](https://wzfou.com/vps/)，现在你就可以需要在 VPS 主机上配置好 Docker 环境，这里有一个一键安装 Docker 环境的命令，配置起来非常地简单：[Docker 和 Docker Compose 一键安装脚本 可手动选择安装版本和下载源](https://wzfou.com/question/101224/)。

### 1.3 一键安装

**仅适用于 Linux amd64/arm64 平台。**

安装：

```
curl -fsSL "https://alist.nn.ci/v3.sh" | bash -s install
```

更新：

```
curl -fsSL "https://alist.nn.ci/v3.sh" | bash -s update
```

卸载：

```
curl -fsSL "https://alist.nn.ci/v3.sh" | bash -s uninstall
```

**自定义路径：**

默认安装在 `/opt/alist` 中。 自定义安装路径，将安装路径作为第二个参数添加，必须是绝对路径（如果路径以 alist 结尾，则直接安装到给定路径，否则会安装在给定路径 alist 目录下），如 安装到 `/root`：

```
# Install
curl -fsSL "https://alist.nn.ci/v3.sh" | bash -s install /root
# update
curl -fsSL "https://alist.nn.ci/v3.sh" | bash -s update /root
# Uninstall
curl -fsSL "https://alist.nn.ci/v3.sh" | bash -s uninstall /root
```

### 1.4 Windows 安装

打开 AList Release 下载 Windows 对应的软件。最新版的前端已经和后端打包好了，不用再下载前端文件了。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_26-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_26.png)

```
# 解压下载的文件，得到可执行文件：
unzip alist-xxxx.zip
# 运行程序
.\alist.exe server
# 获得管理员信息
.\alist.exe admin
```

### 1.5 Docker 安装

选择 Docker，可以执行以下命令安装发行版本：

```
docker run -d --restart=always -v /etc/alist:/opt/alist/data -p 5244:5244 -- xhofe/alist:latest
```

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_02-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_02.png)

二、AList 管理使用
------------

### 2.1 登录账号

首先，如果你是用一键安装方法安装的，使用以下命令来获取账号和密码：

```
./alist admin
```

如果是用的 Docker 查看管理员信息：

```
docker exec -it alist ./alist admin
```

然后打开你的 IP：端口，就可以访问到 AList 后台了。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_03-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_03.png)

使用你刚才获取到的账号和密码登录了。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_04-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_04.png)

在用户管理中可以修改你的账号和密码了。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_05-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_05.png)

### 2.2 添加存储

[AList](https://wzfou.com/tag/alist/) 目前支持的网盘存储如下：

> 通用项  
> 本地存储  
> 阿里云盘  
> OneDrive  
> 天翼云盘  
> 谷歌云盘  
> 123 网盘  
> FTP  
> PikPak  
> 对象存储  
> WebDAV  
> 又拍云存储  
> Teambition  
> 分秒帧  
> 中国移动云盘  
> Yandex 云盘  
> 百度网盘  
> 夸克网盘  
> SFTP  
> 迅雷云盘  
> 115 网盘  
> 一刻相册

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_06-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_06.png)

如果你想添加本地存储的话，直接修改根文件夹路径为您要挂载的文件夹的路径。 例如：

> Linux: `/root`
> 
> Windows: `C:`

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_07.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_07.png)

### 2.3 阿里云盘

AList 添加阿里云盘时，要填写令牌和根文件夹，由于阿里云盘 referer 的限制，必须使用移动端 token。 使用桌面 Web 令牌将导致无法下载和预览。 当然，如果你在本地使用或者带宽足够大，你也可以开启代理，让桌面 Web 的 `refresh token` 正常工作。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_08-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_08.png)

**刷新令牌。**按照这个 ：https://github.com/Xhofe/alist/issues/88 在手机上捕获 / 查找日志 (/data/media/0/Android/data/com.alicloud.databox/ 文件 / 日志 / 跟踪 /）。 或者您可以直接进入：https://alist.nn.ci/zh/guide/drivers/aliyundrive.html

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_08_1-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_08_1.png)

**Root folder file_id。**打开阿里云盘官网，点击进入要设置的文件夹时点击 URL 后面的字符串，如 https://www.aliyundrive.com/drive/folder/5fe01e1830601baf774e4827a9fb8fb2b5bf7940。这个文件夹的 file_id 即为 5fe01e1830601baf774e4827a9fb8fb2b5bf7940：

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_09-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_09.png)

有关于阿里云盘使用可以查看：[Aliyundrive 阿里云盘 - 不限速免费网盘 - 支持分享, 手机相册和微信 / QQ 群文件自动备份](https://wzfou.com/aliyundrive/)。

### 2.4 OneDrive

在打开的页面，选择所在区域，点击创建应用。登陆后选择” 注册应用程序”，输入” 名称”，选择” 任何组织目录中的账户和个人”（注意这里不要看位置选择而是看文字，部分人可能是中间那个选项，不要选成单一租户或者其他选项，否则会导致登陆时出现问题），输入重定向 URL 为 https://tool.nn.ci/onedrive/callback ，点击注册即可，然后可以得到 client_id

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_10-680x345.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_10.png)

注册好应用程序之后，选择” 证书和密码”，点击” 新客户端密码”，输入一串密码，选择时间为最长的那个，点击” 添加” （注：在添加之后输入的密码之后会消失，请记录下来 `client_secret` 的值）

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_11-680x314.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_11.png)

选择 “API 权限”，点击 “Microsoft Graph”，在” 选择权限” 中输入 `file`，勾选 `Files.read`（注：Files.read 是只读最小权限，图中权限较大，也同样可以），点击” 确定”。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_12-680x312.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_12.png)[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_13-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_13.png)

其他的网盘可以参考：https://alist.nn.ci/zh/guide/drivers/common.html

三、AList 使用体验
------------

AList 的使用体验界面如下：

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_15-680x329.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_15.png)

支持在线观看视频和听音乐。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_16-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_16.png)[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_17-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_17.png)

[AList](https://wzfou.com/tag/alist/) 支持在线预览 XSL 和 XSLX 表格文档。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_18-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_18.png)

AList 在线预览代码和图片。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_19-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_19.png)[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_20-680x366.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_20.png)

四、AList 域名访问
------------

想要给 AList 绑定域名，你需要一定的 Nginx 或者 Apache 知识，不过如果你用的是 Docker 安装 AList 的话，可以使用神器：[Nginx 反向绑定域名管理工具 - 无需修改 Nginx 规则一键添加反向绑定域名](https://wzfou.com/nginx-docker/)。

五、AList 对象存储
------------

[AList](https://wzfou.com/tag/alist/) 可以添加对象存储来挂载，平时用的亚马逊 S3、各大云存储服务，只要是支持 S3 协议都可以挂载到 AList。

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_14-680x351.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_14.png)

你需要填写以下信息：

> S3 对象存储协议，如 COS、OSS、B2。
> 
> #存储桶：存储桶名
> 
> #Endpoint：Endpoint address
> 
> #Region：地区
> 
> #Access key id：Access key id
> 
> #Secret access key：Secret access key
> 
> #Root folder path：根路径，不填则默认为根目录。

关于对象存储的使用，你可以参考：

1.  [Linode 对象存储管理与使用教程 - 兼容 S3 协议的对象存储价格便宜超大存储](https://wzfou.com/linode-object-storage/)
2.  [十个国内优秀对象云存储服务使用对比 - 用于网站云存储和 CDN 加速](https://wzfou.com/guonei-yuncunchu/)

六、AList WebDAV
--------------

AList 支持使用 WebDAV 的方式挂载，也就是说你可以将 AList 作为中转。各大网盘支持度如下：

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_22.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_22.png)

WebDAV 配置​如下：

> 参数    值  
> 链接    http[s]://domain:port/dav/  
> 主机    domain:port  
> 路径    dav  
> 协议    http/https  
> 端口    同 web 端口  
> 账号    见后台  
> 密码    见后台

电脑上，如果是播放器 PotPlayer，AList WebDAV 挂载如下：

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_23.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_23.png)

如果想将 AList 当成本地硬盘使用，则可以使用 RaiDrive，挂载如下：

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_24.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_24.png)

RaiDrive 使用可以查看：[本地网络磁盘 RaiDrive 挂载 Dropbox,Google Drive,OneDrive 支持 WebDAV,FTP,SFTP](https://wzfou.com/raidrive/)。

Kodi 使用 WebDAV 如下：

[![](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_25.png)](https://wzfou.cdn.bcebos.com/wp-content/uploads/2022/12/alist-pan_25.png)

Kodi 使用如下：[自建 Nextcloud 影音中心: Aria2 离线下载 + PotPlayer 和 Kodi 本地观看](https://wzfou.com/nextcloud-aria2-kodi/)。

七、总结
----

AList 目录列表程序功能，想要长期使用的话建议使用 VPS 主机来搭建，否则也可以直接在 PC 电脑上用命令的方式运行 AList 。

文章出自：[挖站否](https://wzfou.com/) [https://wzfou.com/alist/](https://wzfou.com/alist/)，版权所有。本站文章除注明出处外，皆为作者原创文章，可自由引用，但请注明来源。