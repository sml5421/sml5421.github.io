> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [tidgi.fun](https://tidgi.fun/%E5%A4%AA%E8%AE%B0%E5%8A%9F%E8%83%BD%E6%89%8B%E5%86%8C%2F%E5%BC%80%E5%90%AF%20HTTP%20API)

太记功能手册 / 开启 HTTP API
--------------------

[林一二](%E6%9E%97%E4%B8%80%E4%BA%8C) 2023 年 09 月 02 日 23:01[太记功能手册](%E5%A4%AA%E8%AE%B0%E5%8A%9F%E8%83%BD%E6%89%8B%E5%86%8C)

开启方法
----

在太记侧边栏上：

右键工作区图标 - 配置工作区 - 博客和服务器设置 - 启用 HTTP API

开启的作用
-----

可以使用 [TW-MobiLe-Sync 手机 tiddloid 移动端同步 TidGi 桌面端插件](https://tw-cn.netlify.app/#TW-MobiLe-Sync%E6%89%8B%E6%9C%BAtiddloid%E7%A7%BB%E5%8A%A8%E7%AB%AF%E5%90%8C%E6%AD%A5TidGi%E6%A1%8C%E9%9D%A2%E7%AB%AF%E6%8F%92%E4%BB%B6)了，因为它是用 HTTP API 来同步数据的。

可以开博客了，参考[在手机上运行太微 nodejs 博客](https://wiki.onetwo.ren/%E5%9C%A8%E6%89%8B%E6%9C%BA%E4%B8%8A%E8%BF%90%E8%A1%8C%E5%A4%AA%E5%BE%AEnodejs%E5%8D%9A%E5%AE%A2)，或[太记功能手册 / 通过内网穿透开设博客](%E5%A4%AA%E8%AE%B0%E5%8A%9F%E8%83%BD%E6%89%8B%E5%86%8C%2F%E9%80%9A%E8%BF%87%E5%86%85%E7%BD%91%E7%A9%BF%E9%80%8F%E5%BC%80%E8%AE%BE%E5%8D%9A%E5%AE%A2)。

可以和第三方应用互相同步数据，如果第三方应用适配了太记 HTTP API 的话。

注意安全
----

开启后，同一个 Wifi 局域网里的其他人都能访问你的笔记，所以这个功能默认关闭。使用需要注意信息安全！

### 报错 401

如果开启了「凭证鉴权」功能，就会报这个错，401 意思就是凭证无效拒绝访问。「凭证鉴权」功能需要懂 Web 技术才能用，但是能大大增加安全性。