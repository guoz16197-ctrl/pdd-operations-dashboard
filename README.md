# 拼多多运营工作台

静态 GitHub Pages 站点。网页入口为 `index.html`。

## 自动同步

- `sync-pdd-data.ps1` 通过本机已登录的 `pdd-mms` 专用 Chrome 拉取商品、库存、活动和营销工具数据。
- Windows 计划任务每 2 分钟执行一次；仅当业务数据发生变化时提交并推送 `data.json`。
- 页面每 2 分钟重新读取一次 `data.json`。
- 电脑关机、调试端口 `9222` 未启动或拼多多登录过期时不会更新，错误记录在 `PDD-MMS-MCP/logs/github-pages-sync.log`。
