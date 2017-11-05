# Permissions

权限或者是一个名字，或者是一个 match pattern

- [Declare Permissions](https://developer.chrome.com/extensions/declare_permissions)
- [Match Patterns](https://developer.chrome.com/extensions/match_patterns)

chrome.* APIs 文档会告知需要什么权限。

有些权限，在用户安装扩展会给出警告，比如 `<all_urls>`。

## activeTab

[The activeTab permission](https://developer.chrome.com/extensions/activeTab)

extension manifest:

```json
"permissions": [
  "activeTab"
],
```

`activeTab` 临时获得对当前 tab 的操作权限

- 访问 tabs.Tab 的 url, title, favIconUrl
- 使用 tabs.executeScript, tabs.insertCSS
