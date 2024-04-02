> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [ld246.com](https://ld246.com/article/1692089679062?r=a2930610542)

> 一、前言 我自己折腾了很久才搞明白，写下这篇教程既是避免自己忘记操作，也是为了帮助后来者节省时间。

一、前言
----

我自己折腾了很久才搞明白，写下这篇教程既是避免自己忘记操作，也是为了帮助后来者节省时间。

所以，请你在有以下需求的前提下阅读本教程，否则更应该把折腾工具的时间花在多写一些笔记上。

*   多设备同步的需求
*   省钱的需求

如果你绝大多数时候只在一台设备上使用思源笔记，更简单的做法是不必执着于同步笔记，更应该定期手动导出 Data 文件备份。其他时候记笔记可以使用 `微信文件传输助手` 、 `手机备忘录` 等应急 ，过后再整理到思源笔记。

如果比起省一些钱，你更在意少花点时间折腾，请直接 [`年付订阅`](https://ld246.com/forward?goto=https%3A%2F%2Fb3log.org%2Fsiyuan%2Fpricing.html%3Fr%3Da2930610542) ，使用官方云同步服务。

### ※ 注意，以下是使用该教程方法的必要条件

*   愿意为第三方存储功能与对象存储付费
*   有绑定了你身份证信息的支付宝
*   可以使用电脑

二、省钱，但无法免费
----------

1.  思源笔记第三方存储功能（功能特性）[（点此进入定价页面）](https://ld246.com/forward?goto=https%3A%2F%2Fb3log.org%2Fsiyuan%2Fpricing.html%3Fr%3Da2930610542)
    
    *   可接入第三方云端存储（S3/WebDAV）的 **功能特性已经收费**（从 2024 年 1 月，v2.12.0 版本开始），**一次付费后终身可用**（订阅会员包含了功能特性，在会员有效期内不需要为此单独付费）
    *   目前打折价 64 元：[https://b3log.org/siyuan/pricing.html](https://ld246.com/forward?goto=https%3A%2F%2Fb3log.org%2Fsiyuan%2Fpricing.html%3Fr%3Da2930610542)
2.  青云 QingCloud 对象存储（**很便宜**的，不用担心）[（点此进入资费介绍页面）](https://ld246.com/forward?goto=https%3A%2F%2Fdocsv4embed.qingcloud.com%2Fuser_guide%2Fstorage%2Fobject_storage%2Fbilling%2Fprice%2F)
    
    *   **免费额度**
        
        注册成功并完成认证的 QingStor 对象存储用户，青云 QingCloud 为您提供一定额度的 QingStor 对象存储免费使用套餐。每个 Bucket 享有如下免费政策:
        
        *   标准存储空间：20 GB
        *   总外网下载流量：10 GB
        *   总外网读请求 (GET/HEAD)：100 万次
        *   总外网写请求 (PUT/POST/DELETE)：10 万次
    *   按量计费
        
        *   存储费用：存储总量 10GB 内免费，超过后阶梯计费，在 10GB-1TB 内 0.147 元 / GB / 月
        *   流量费用：每月下载流量 1GB 内免费，超过后阶梯计费，在 1GB-3TB 内 0.45 元 / GB / 月
        *   API 请求费用：0.01 元 / 万次
    *   对象存储的计费周期为月，每月初会根据用量自动扣除上个月费用。若当月费用扣除后余额不足，则用户的所有存储空间将会处于 `暂停` 状态，此时用户无法使用对象存储的任何功能。等到用户充值足够的金额后，用户的所有存储空间将会自动恢复。
        
        *   建议在确认同步功能可以正常使用后至少充值 1 元（最低充值金额）：[点此进入青云充值页面](https://ld246.com/forward?goto=https%3A%2F%2Fconsole.qingcloud.com%2Fbilling%2Fwallet%2F)

三、以下是详细教程，但碰到意外情况需要自己想办法
------------------------

1. 确保你可以使用思源笔记的第三方存储功能
----------------------

如果你还没有付费，可以先免费试用订阅，也可以直接升级 `功能特性` 或 `年付订阅` ：[https://b3log.org/siyuan/pricing.html](https://ld246.com/forward?goto=https%3A%2F%2Fb3log.org%2Fsiyuan%2Fpricing.html%3Fr%3Da2930610542)

当然，如果你已升级 [`年付订阅`](https://ld246.com/forward?goto=https%3A%2F%2Fb3log.org%2Fsiyuan%2Fpricing.html%3Fr%3Da2930610542) ，在官方云存储剩余容量足够的前提下，不妨直接使用思源官方云同步服务。

页面如下：

1.  打开 SiYuan `设置` 页面，点击 `云端`
2.  **云端存储服务提供商** 选择 `S3`

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230814130717-jhaybw4.png?imageView2/2/interlace/1/format/webp)

2. 注册青云
-------

#### 注意，帖子最初写于 2023 年，如果注册流程在之后有变化，请随机应变。

使用电脑浏览器在[这个页面](https://ld246.com/forward?goto=https%3A%2F%2Faccount.qingcloud.com%2Fsignup)注册：[https://account.qingcloud.com/signup](https://ld246.com/forward?goto=https%3A%2F%2Faccount.qingcloud.com%2Fsignup)

_用电脑浏览器是因为：经我实测，实名认证时通过手机扫描二维码无法上传图片，使用手机浏览器也无法上传图片。为了避免你折腾半天也上传不了图片，建议你优先尝试用电脑浏览器完成以下全部流程。_

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815062627-l5wbz03.png?imageView2/2/interlace/1/format/webp)

注册成功后可以 `选择币种` 和 `实名认证`

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815113029-kkcjwbj.png?imageView2/2/interlace/1/format/webp)

3. 在电脑网页上完成实名认证
---------------

1.  注册成功后点击上图框选出来的 `立即认证` ，或者打开[这个页面](https://ld246.com/forward?goto=https%3A%2F%2Fconsole.qingcloud.com%2Faccount%2Fprofile%2Fadvanced)（账户中心 - 认证信息）：[https://console.qingcloud.com/account/profile/advanced](https://ld246.com/forward?goto=https%3A%2F%2Fconsole.qingcloud.com%2Faccount%2Fprofile%2Fadvanced)
2.  **分别**准备自己的身份证**人像面**与**国徽面**图片文件，可以手机拍照（尽量正着拍照，太歪可能无法识别）并裁切合适范围后发送图片到电脑，注意保存图片文件至容易找的目录（比如临时放在电脑桌面上）
3.  点击 `支付宝快速认证` **分别**上传身份证**人像面**与**国徽面**图片文件（注意满足上传格式要求）
4.  下面的姓名和身份证号信息会在上传身份证照片后自动识别填写，识别有错误需要手动修改
5.  按 `提交` 按钮
6.  使用绑定了你身份证信息的支付宝扫码，在手机上进行验证，认证完毕后点击 `我已完成认证`
7.  可以看到认证状态变为 `已认证`

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815113557-jsqo4q0.png?imageView2/2/interlace/1/format/webp)

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815113829-ubtzdu2.png?imageView2/2/interlace/1/format/webp)

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815151830-awrp2xz.png?imageView2/2/interlace/1/format/webp)

4. 创建存储桶（Bucket）并设置
-------------------

1.  打开[对象存储页面](https://ld246.com/forward?goto=https%3A%2F%2Fconsole.qingcloud.com%2Fgd2%2Fqingstor%2F)：[https://console.qingcloud.com/gd2/qingstor/](https://ld246.com/forward?goto=https%3A%2F%2Fconsole.qingcloud.com%2Fgd2%2Fqingstor%2F)
    
2.  在页面上方**就近**选择区域（比如我选择广东 2 区）
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815152714-08maq4c.png?imageView2/2/interlace/1/format/webp)
    
3.  创建存储桶（Bucket）
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815153018-r5rxhp1.png?imageView2/2/interlace/1/format/webp)
    
4.  设置存储桶（Bucket）名称，点击 `确定`
    
    *   Bucket 名称在 Qingstor™ 对象存储中是全局唯一的，只要这个名称的存储桶（Bucket）没有被任何人创建过，你可以使用你喜欢的任意名称；如果你不想思考名称，可以参照我的格式创建：`siyuan-电话号码`
        
        ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815115045-uci7x5m.png?imageView2/2/interlace/1/format/webp)
        
5.  鼠标移动到新建的存储桶（Bucket）上，右键单击，点击 `复制 Bucket URL` ，先临时粘贴到某个地方，待会要用
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815154701-zljezge.png?imageView2/2/interlace/1/format/webp)
    
6.  鼠标移动到新建的存储桶（Bucket）上，右键单击，点击 `设置`
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815153457-3m2hm5m.png?imageView2/2/interlace/1/format/webp)
    
7.  **（如果你知道这是什么并且需要的话）** 启用版本管理
    
    ![](https://b3logfile.com/file/2023/11/image-XoNKPtU.png?imageView2/2/interlace/1/format/webp)
    
8.  **（如果你知道这是什么并且需要的话）** 生命周期管理添加规则（按照下图顺序进行设置）
    
    ![](https://b3logfile.com/file/2023/11/image-ENZgIur.png?imageView2/2/interlace/1/format/webp)
    
    ![](https://b3logfile.com/file/2023/11/image-hpmq0w5.png?imageView2/2/interlace/1/format/webp)
    
    _这个要一次性设置好，否则你再次进入设置界面时，操作对象会默认给你改为 `对当前版本操作`，到时候文件被删了就麻烦了_
    

‍

5. 创建 API 密钥
------------

1.  在页面右上角打开 `API 密钥` ，或者[访问此页面](https://ld246.com/forward?goto=https%3A%2F%2Fconsole.qingcloud.com%2Faccess_keys%2F)
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815155515-56q8by1.png?imageView2/2/interlace/1/format/webp)
    
2.  创建 API 密钥
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815155750-7481fkz.png?imageView2/2/interlace/1/format/webp)
    
3.  填写**名称**和**描述**后提交![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815155927-ayaunyf.png?imageView2/2/interlace/1/format/webp)
    
4.  及时下载（只有一次下载机会），找一个位置保存文件，并妥善备份
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815160134-nrk6vzd.png?imageView2/2/interlace/1/format/webp)
    
5.  使用记事本打开文件（文件名为 `access_key.csv`），在单引号内的字符串（不包括单引号）分别对应着 Acess Key 和 Secret Key
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815160714-0304ddm.png?imageView2/2/interlace/1/format/webp)
    

6. 配置 SiYuan 云端设置
-----------------

1.  打开 SiYuan `设置` 页面，点击 `云端`
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230814130717-jhaybw4.png?imageView2/2/interlace/1/format/webp)
    
2.  **云端存储服务提供商** 选择 `S3`
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815130727-6qm0ymj.png?imageView2/2/interlace/1/format/webp)
    
3.  **Endpoint** 输入访问地址（格式大致为：`https://s3.<zone-id>.qingstor.com/`）
    
    输入访问地址的流程如下：
    
    *   在第 4 步的第 5 小步你得到了 `Bucket URL` ，现在把它复制一下
    *   然后粘贴在 **Endpoint** 中，并将存储桶的名称部分（ `<bucket-name>` ）改为 `s3` 。比如我设置的存储桶名称是：`siyuan-12345678901` ，那么就将 `https://siyuan-12345678901.gd2.qingstor.com` 改为 `https://s3.gd2.qingstor.com/` 。（注意链接中字母是小写，不要错了）  
        ![](https://b3logfile.com/file/2024/02/image-BtPl998.png?imageView2/2/interlace/1/format/webp)
    
    注：本教程使用 Path Style（风格）的访问地址，所以格式大致为：`http://s3.<zone-id>.qingstor.com`。其中，`<zone-id>` 是指你在第 4 步创建存储桶时选择的区域所对应的代码，你可以参照下图表格填写，当然最简单的是按照前述的方法复制粘贴。
    
    [官方文档](https://ld246.com/forward?goto=https%3A%2F%2Fdocsv4.qingcloud.com%2Fuser_guide%2Fstorage%2Fobject_storage%2Fintro%2Fproduct%2F%23_%25E5%259F%25BA%25E6%259C%25AC%25E6%25A6%2582%25E5%25BF%25B5)内容：
    
    ![](https://b3logfile.com/file/2024/02/image-w2e4TRu.png?imageView2/2/interlace/1/format/webp)
    
4.  **Acess Key** 输入你在第 5 步第 5 小步获取的 qy_access_key_id
    
5.  **Secret Key** 输入你在第 5 步第 5 小步获取的 qy_secret_access_key
    
6.  **Bucket** 输入你的存储桶名称，如我的 `siyuan-12345678901`
    
7.  **Region** 输入区域代码，按照上图或官方文档的 `Region ID` 列来填写，没有的话应该可以不填，但我还是按照自己的区域输入了 `gd2`
    
8.  **Addressing** 选项改为 `Path-style`
    
9.  **TLS Verify** 默认
    
10.  开启 **启用云端同步**
    
11.  开启 **同步冲突时生成冲突文档**
    
12.  **云端同步模式** 按照需求设置：
    
    *   自动同步（数据不再变动后 30 秒进行一次同步）
    *   手动同步（仅启动和关闭软件时自动同步一次，其他时候需要手动触发同步）
    *   完全手动同步（启动和关闭时均不同步，完全手动控制同步时机和同步方向）
13.  点击 **云端同步目录** 右侧 `设置` ，可见账户下所有 S3 存储桶，点击目标存储桶即可
    

7. 尝试同步
-------

### ※ 注意，在使用同步功能前请认真了解[《思源笔记同步指南》](https://ld246.com/article/1683395267749?r=a2930610542)中的内容，这关乎你的笔记数据安全

### ※ 注意，在使用同步功能前请认真了解[《思源笔记同步指南》](https://ld246.com/article/1683395267749?r=a2930610542)中的内容，这关乎你的笔记数据安全

### ※ 注意，在使用同步功能前请认真了解[《思源笔记同步指南》](https://ld246.com/article/1683395267749?r=a2930610542)中的内容，这关乎你的笔记数据安全

1.  导出 Data 备份好
    
    ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815162115-ogq9rx8.png?imageView2/2/interlace/1/format/webp)
    
2.  手动点击一次同步图标进行同步，如果报错，请自行定位问题。
    
    _你可以对照教程看看哪一步做错了，也可以复制报错信息去 “GPT 一下”，还可以在链滴上提问…_
    
3.  判断是否上传成功
    
    *   双击进入存储桶，打开 _**repo**_ 文件夹，能见到 _**repo**_ 文件夹下的文件
        
        ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815162828-qo8s4os.png?imageView2/2/interlace/1/format/webp)
        
    *   如果你是第一次使用 S3 同步的话，理论上空间大小应该与手动导出的 Data 文件大小差不太多
        
        ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815162958-ckcvety.png?imageView2/2/interlace/1/format/webp)
        
    *   ![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815163208-ta8gf7h.png?imageView2/2/interlace/1/format/webp)
        
4.  在需要同步的另一台设备上按照第 6 步，填写同样的配置（**云端同步模式**可以不同）
    
    *   建议在使用频次较低的设备上使用 `完全手动同步模式` ，每一次使用时通过 `下载云端数据快照` 同步从另一台设备上传的云端数据，避免数据冲突。需要注意的是：这样做并不代表你可以在多台设备上同时修改笔记，更好的方法是养成习惯：在切换设备前手动点击同步图标，等待数据完全同步至云端后关闭软件，之后再切换设备下载云端数据。
    *   建议在第一次尝试使用第三方同步功能时，在所有的设备上都使用 `完全手动同步模式` ，能有效避免误操作覆盖数据
5.  在一台设备的思源笔记 `上传本地数据快照` 后，在另一台设备中的思源笔记 `下载云端数据快照` （不要选错，否则数据就被覆盖了）
    

8. 绑定微信、邮箱账号（不是必要的，但建议）
-----------------------

在 [账户中心 - 基本信息](https://ld246.com/forward?goto=https%3A%2F%2Fconsole.qingcloud.com%2Faccounts%2Fprofile%2Fbasic%2F) 绑定你的其他账号：[https://console.qingcloud.com/accounts/profile/basic/](https://ld246.com/forward?goto=https%3A%2F%2Fconsole.qingcloud.com%2Faccounts%2Fprofile%2Fbasic%2F)

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815123541-rv6owbc.png?imageView2/2/interlace/1/format/webp)

9. 按需充值
-------

进入存储桶，在上方选择 `消费记录` 页面可以查看 `本月预估费用`

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815124414-5okkhy7.png?imageView2/2/interlace/1/format/webp)

对象存储的计费周期为月，每月初会根据用量自动扣除上个月费用。若当月费用扣除后余额不足，则用户的所有存储空间将会处于 `暂停` 状态，此时用户无法使用对象存储的任何功能。等到用户充值足够的金额后，用户的所有存储空间将会自动恢复。

以下是最新（2024-02-10）的[费用标准](https://ld246.com/forward?goto=https%3A%2F%2Fdocsv4embed.qingcloud.com%2Fuser_guide%2Fstorage%2Fobject_storage%2Fbilling%2Fprice%2F)：

> *   免费额度  
>     注册成功并完成认证的 QingStor 对象存储用户，青云 QingCloud 为您提供一定额度的 QingStor 对象存储免费使用套餐。每个 Bucket 享有如下免费政策:
>     *   标准存储空间：20 GB
>     *   总外网下载流量：10 GB
>     *   总外网读请求 (GET/HEAD)：100 万次
>     *   总外网写请求 (PUT/POST/DELETE)：10 万次
> *   按量计费
>     *   存储费用：存储总量 10GB 内免费，超过后阶梯计费，在 10GB-1TB 内 0.147 元 / GB / 月
>     *   流量费用：每月下载流量 1GB 内免费，超过后阶梯计费，在 1GB-3TB 内 0.45 元 / GB / 月
>     *   API 请求费用：0.01 元 / 万次

另外值得注意的是，在[《第三方同步选择 - S3 服务商对比推荐》](https://ld246.com/article/1668672970787)一文中提供的超链接内容可能已经过时

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815125955-s3po6t5.png?imageView2/2/interlace/1/format/webp)

最新的 [资费介绍页面](https://ld246.com/forward?goto=https%3A%2F%2Fdocsv4embed.qingcloud.com%2Fuser_guide%2Fstorage%2Fobject_storage%2Fbilling%2Fprice%2F) 在：[https://docsv4embed.qingcloud.com/user_guide/storage/object_storage/billing/price/](https://ld246.com/forward?goto=https%3A%2F%2Fdocsv4embed.qingcloud.com%2Fuser_guide%2Fstorage%2Fobject_storage%2Fbilling%2Fprice%2F)

建议在同步功能正常使用后按需充值（最低充值金额为 1 元）：[点此进入青云充值页面](https://ld246.com/forward?goto=https%3A%2F%2Fconsole.qingcloud.com%2Fbilling%2Fwallet%2F)

‍

**END**
-------

p.s.

*   除了青云，你也可以选择其他的服务商。关于服务商的选择可以参考这篇文章：[《第三方同步选择 - S3 服务商对比推荐》](https://ld246.com/article/1668672970787?r=a2930610542) ，不过**具体的数据很可能已经过时**，需要留意；各个厂商的配置方法大同小异。
*   使用 S3 同步只会同步工作空间下的 _**repo**_ 文件夹（里面是经过加密的文件，实际上已经包含了整个工作空间），如需单独同步工作空间目录下的某些文件或文件夹，请在关闭思源笔记后手动复制到其他设备。

如果本篇教程对你有帮助，能否请你点击本帖右下角，给我一个大大的感谢以及一个免费的赞同，还可以分享给需要的朋友。你的鼓励与支持就是我创作的最大动力。

![](https://b3logfile.com/file/2023/08/siyuan/1672108273034/assets/image-20230815150538-rjykz20.png?imageView2/2/interlace/1/format/webp)

‍「友情链接」：[【代码片段分享】思源笔记用到现在积累的所有代码片段](https://ld246.com/article/1700551933609?r=a2930610542)