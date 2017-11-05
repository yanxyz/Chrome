# Incognito

在扩展管理页面，在目标扩展，勾选“在隐身模式下启用”，让此扩展可以在隐身窗口下使用。
浏览器会给出警告，“扩展会记录你的记录”。

## Manifest

- [Manifest - Incognito](https://developer.chrome.com/extensions/manifest/incognito)

extension manifest:

```json
"incognito": "spanning"
```

默认值 "spanning" 意思是，扩展运行在共享进程中，来自 incognito tab 的消息将发送到这个共享进程，同时以一个标志 `incognito` 表示消息的来源。 incognito tab 不能使用这个共享进程，extension pages 不能在 incognito window 打开。

"split" 意思是，extension pages 运行在 incognito process。

## Api

- [chrome.extension](https://developer.chrome.com/extensions/extension)

`inIncognitoContext` 判断 content scripts 是否运行在 incognito tab， extension 是否运行在 incognito process。

`isAllowedIncognitoAccess` 判断用户是否勾选 “在隐身模式下启用”。
