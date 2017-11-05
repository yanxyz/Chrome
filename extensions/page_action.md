# Page Actions

- [chrome.pageAction](https://developer.chrome.com/extensions/pageAction)

类似于 browser actions, page actions 有 icon, tooltip, popup，但是不能有 badges。

extension manifest:

```json
"page_action": {
  "default_icon": {},
  "default_title": "",  // tooltip
  "default_popup": "popup.html",  // popup page
}
```

点击 page action icon 时，如果有 popup page 则显示它，如果没有则触发 chrome.pageAction.onClicked 事件。

page action icon 默认为灰色，表示当前页面不可用 page action。可以用 `pageAction.show()`, `pageAction.hide()` 控制它的状态。

chrome 48 开始，page action icon 不再放在地址栏中，而是跟 browser action icon 一样放在工具栏中（地址栏右边是工具栏），这个改变让 page action 有些鸡肋。

- https://productforums.google.com/forum/#!msg/chrome/wOUFbsKqPg0/f4jJ2K9bCgAJ


