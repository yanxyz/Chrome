# Options page

扩展配置页面

[Options](https://developer.chrome.com/extensions/options)

extension manifest:

```json
"options_page": "options.html"
```

使用 [storage.sync](https://developer.chrome.com/extensions/storage#property-sync) API 保存配置，而且可以同步保存到服务器。

## Options v2

[Options v2](https://developer.chrome.com/extensions/optionsV2)

extension manifest:

```json
"options_ui": {
  "page": "options.html",
  "chrome_style": true
}
```

打开 options page 时，v1 是新建一个标签页面，v2 是以扩展管理页面对话框的形式（Shadow DOM 技术）。如果配置页面比较简单，可以考虑 v2。
