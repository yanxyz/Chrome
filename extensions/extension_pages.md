# Extension pages

Extension pages 运行在同一个进程中，`chrome.extension.getViews` 获取相应的 window，从而可以使用其它页面的函数，修改其它页面 DOM。

- background page
- popup page
- option page
- override page

可以类比框架页面，background page 是 top frame，其它页面是 sub frame。
