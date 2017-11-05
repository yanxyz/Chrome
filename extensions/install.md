# 安装 Chrome 扩展

从 [chrome web store](https://chrome.google.com/webstore/category/extensions?hl=en-US) 安装扩展，需要代理。

从第三方网站下载扩展（注意有安全风险）

- <https://chrome-extension-downloader.com/>
<!-- - <https://www.chromefor.com/get_extensions/> -->

下载得到的 `.crx` 文件如何安装呢？见下文

## 安装本地扩展 {#unpacked}

通过开发者模式可以安装本地扩展(`.crx` 文件或包含 `manifest.json` 的目录)。

注意：只有 Chrome dev/canary 版本可以这么做。

在扩展管理页面开启开发者模式

![](../images/extension-developer-mode.png)

然后把扩展拖到这个页面安装。

以这种方式安装的扩展，在启动 Chrome 时会提示停用这些扩展

![](../images/extension-alert.png)
