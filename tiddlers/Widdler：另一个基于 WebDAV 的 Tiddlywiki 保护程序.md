[](#a-webdav-server-for-tiddlywikis-1)TiddlyWikis 的 WebDAV 服务器
--------------------------------------------------------------

在 Windows 10（64 位）  
上快速启动 这也应该适用于其他系统

1.  下载您选择的二进制文件，适用于 Win 10 64b  
    1.1。转到[发布 v1.2.1 ·qbit/widdler ·GitHub上 5](https://github.com/qbit/widdler/releases/tag/v1.2.1)  
    1.2. 下载[widdler\_1.2.1\_Windows\_x86\_64.tar.gz 1](https://github.com/qbit/widdler/releases/download/v1.2.1/widdler_1.2.1_Windows_x86_64.tar.gz)
2.  解压缩到您选择的文件夹中`widdler_1.2.1_Windows_x86_64.tar.gz`
3.  打开 shell 窗口（如 powershell 或 cmd 命令窗口）
4.  运行此操作将生成一个文件  
    4.1。提供选择  
    的用户名 4.2.提供密码`widdler.exe -gen``.htpasswd`
5.  通过输入 At Prompt 来运行 Widdler`widdler.exe`
6.  打开浏览器并输入`http://localhost:8080/`

仅此而已

6.  如果你想创建一个新的wiki，只需指出它，Widdler将即时创建一个新的wiki，就像

*   `http://localhost:8080/wiki.html`将从 Tiddlywki 5.2.1 创建wiki.html
*   `http://localhost:8080/hirad.html`将从 Tiddlywki 5.2.1 创建hirad.html