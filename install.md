# 安装 Chrome 浏览器

如果从 [官网](https://www.google.com/chrome/) 下载安装程序，需要代理，而更新也需要代理。

如果使用[电脑管家](https://pc.qq.com)等软件管理工具，它们提供 Chrome 安装，并且可以自动更新。

## My solution

首先从软件下载网站下载安装程序

- [sina](http://down.tech.sina.com.cn/page/40975.html)。

选择 dev 版本下载。

然后安装扩展 [crx-chrome-sina](https://github.com/yanxyz/crx-chrome-sina/)，平常点一下扩展图标检查更新。

对于 Chrome dev/beta/stable 版本，大概六个星期发布一个新版本，所以手工检查更新是可以接受的。
而对于 Chrome Canary 版本，它更新频繁，手工更新不合适。

## Portable

我使用 portable 主要是为了测试不同的 Chrome 版本。

方法一，使用第三方的（注意安全风险）

- [Google Chrome Portable](http://portableapps.com/apps/internet/google_chrome_portable)

方法二，借助 Chrome 的命令行选项，自己制作 portable。
Windows 下可以尝试我写的工具 [ChromeLnk](https://github.com/yanxyz/ChromeLnk/)。
可以为 Chrome 创建不同的快捷方式，用于不同的用途，比如

- `Chrome.lnk` 开发用
- `ChromeYan.lnk` 日常用
