# browser action

- [chrome.browserAction](https://developer.chrome.com/extensions/browserAction)

extension manifest:

```json
"browser_action": {
  "default_icon": {},
  "default_title": "",  // tooltip
  "default_popup": "popup.html",  // popup page
}
```

browser action icon 位于工具栏中（地址栏右边）。

点击 browser action icon，如果有 popup page 则显示它，如果没有则触发 `browserAction.onClicked` 事件。

browser action 默认启用，browser action icon 不是灰色的。可以用 `browserAction.enable()`, `browserAction.disable()` 控制它的状态。
