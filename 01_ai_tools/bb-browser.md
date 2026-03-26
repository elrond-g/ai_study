# bb-browser

"浏览器即 API" — 为 AI Agent 提供的 CLI 和 MCP Server，可控制 Chrome 浏览器，复用真实登录状态访问网站。

## 核心特性

- **36 平台 103 条命令**：覆盖 Twitter、Reddit、YouTube、知乎、Bilibili、LinkedIn、GitHub 等
- **浏览器命令**：open、snapshot、click、fill、eval、fetch、network 请求、截图
- **真实登录态**：直接使用浏览器已有登录状态操作网站，无需管理 cookie/token
- **MCP Server**：标准 MCP 协议，可供 Claude Code 等 AI Agent 直接调用
- **CDP 直连**：通过 Chrome DevTools Protocol 直接管理 Chrome 实例
- **适配器系统**：平台适配器维护在 bb-sites 仓库，可扩展

## 链接

- GitHub: https://github.com/epiral/bb-browser
