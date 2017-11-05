# background

## Event Pages

[Event Pages](https://developer.chrome.com/extensions/event_pages)

Chrome 22 引入 Event pages。Event pages 在需要时加载，在空闲时卸载。

extension manifest:

```json
"background": {
    "scripts": ["eventPage.js"],
    "persistent": false
}
```

如果不指定 `"persistent": false` 则是普通的 background page。

可以在 Chrome task manager（`Shift + Esc`） 观察 event page 的生命周期。在扩展管理页面（启用开发者模式）可以看到 background page 的活动状态。

Event page 卸载之后，有些任务无法运行

- window.setTimeout() window.setInterval(), 可用 chrome.alarms API
- extension.getBackgroundPage 换为 runtime.getBackgroundPage，后者是异步方法。

