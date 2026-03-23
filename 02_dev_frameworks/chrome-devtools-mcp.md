# chrome-devtools-mcp

> ⭐ 30,996 | TypeScript | https://github.com/ChromeDevTools/chrome-devtools-mcp | https://npmjs.org/package/chrome-devtools-mcp

## 项目简介

chrome-devtools-mcp 是 Chrome DevTools 团队官方出品的 MCP 服务器，让 AI Agent（Claude Code 等）通过 MCP 协议直接操控 Chrome 浏览器的开发者工具。Agent 可以访问 DOM、执行 JavaScript、截图、分析性能、调试网络请求——一切 DevTools 能做的事 AI 都能做。

## 核心功能

- **DOM 操作**：通过 AI 指令查询和修改页面 DOM 结构
- **JavaScript 执行**：在页面上下文中运行任意 JS 代码
- **网络监控**：拦截和分析 HTTP 请求/响应
- **截图功能**：捕获页面或特定元素的截图
- **性能分析**：获取页面加载和运行时性能数据
- **Puppeteer 集成**：支持通过 Puppeteer 控制浏览器

## 技术特点

- MCP Server 标准实现，与任何 MCP 客户端兼容
- 基于 Chrome DevTools Protocol（CDP）
- 支持 Headless 和有头浏览器两种模式

## 快速开始

```bash
npx chrome-devtools-mcp
# 在 Claude Code 的 MCP 配置中添加此服务器
```

## 使用场景

- AI Agent 自动化前端开发和调试流程
- 让 Claude Code 直接在浏览器中验证生成的代码
- 构建能够操控真实浏览器的 AI 测试工具

## 相关链接

- GitHub: https://github.com/ChromeDevTools/chrome-devtools-mcp
- npm: https://npmjs.org/package/chrome-devtools-mcp
