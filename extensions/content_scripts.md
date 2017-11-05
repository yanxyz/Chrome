# Content Scripts

[Content Scripts](https://developer.chrome.com/extensions/content_scripts)

扩展要获取 web pages 的数据或修改 web pages，需要借助 content scripts。将 content scripts 插入 web pages 之后, 由于它运行在 web pages 上，所以它能操作 web pages。

## 插入页面

方式一，让 Chrome 自动插入。

extension manifest

```json
"content_scripts": [
  {
    "matches": [ "http://www.google.com/*" ],
    "css": [ "mystyles.css" ],
    "js": [ "jquery.js", "myscript.js" ]
  }
]
```

方式二，手工插入，即通过 `tabs.executeScript`, `tabs.insertCSS` 插入。

extension manifest

```json
"permissions": [
  "tabs", // 获取 `tabs.executeScript`, `tabs.insertCSS` 权限
  "http://www.google.com/*" // 获取跨域权限
]
```

如果只插入当前标签页，`activeTab` 即可。

- [Requesting cross-origin permissions](https://developer.chrome.com/extensions/xhr#requesting-permission)


## 运行环境

Content scripts 运行环境是孤立的，与外界隔绝。

只能使用少数的 chrome.* APIs。

### 与 extension pages 交互

Content scripts 运行在 web pages 而不是 extension pages，不能使用 extension pages 的变量和函数。

[message](https://developer.chrome.com/extensions/messaging)

- chrome.runtime.onMessage
- chrome.runtime.connect

extension pages 使用 chrome.tabs.sendMessage 向指定 tab 内的 content scripts 发送消息。

```js
// extension pages
chrome.tabs.sendMessage(tabId, message, callback)
// content scripts
chrome.runtime.onMessage.addListener(function (message, sender, sendResponse) {})
```

content scripts 使用 chrome.runtime.sendMessage 向 extension pages 发送消息。

```js
// content scripts
chrome.runtime.sendMessage(extensionId, message, callback)
// extension pages
chrome.runtime.onMessage.addListener(function (message, sender, sendResponse) {})
```

### 与 web pages 交互

Content scripts 与 web pages scripts 和其它扩展的 content scripts 隔绝，所以不能使用它们的变量和函数，不过共享 web pages DOM。

### 调试

web pages 打开开发者工具，打开 Sources 面板，可以看到 "Content scripts"。
