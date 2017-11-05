# Manifest File

扩展必须有一个文件 manifest.json

[Manifest File Format](https://developer.chrome.com/extensions/manifest)

## Manifest V2

chrome 18 开始应当指定

```json
"manifest_version": 2
```

[Tutorial: Migrate to Manifest V2](https://developer.chrome.com/extensions/tut_migration_to_manifest_v2)

## icons

[Manifest - Icons](https://developer.chrome.com/extensions/manifest/icons)

扩展的图标，最好是 PNG 格式，可以半透明。

- 128x128 用于应用商店，必选
- 48x48 用于扩展管理页面 chrome://extensions
- 16x16 用于 extension pages favicon，contextMenu
