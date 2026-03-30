# web-access

> ⭐ 1.8k+ | Node.js + CDP | https://github.com/eze-is/web-access | MIT

## 项目简介

web-access 是为 Claude Code 设计的高级联网 Skill，提供完整的浏览器自动化能力。核心设计思想"像人一样思考"，三层通道调度机制智能选择最佳访问方式。

## 三层通道调度

| 层级 | 方式 | 场景 |
|------|------|------|
| 第一层 | WebSearch | 轻量级网络搜索 |
| 第二层 | WebFetch | 网页内容抓取 |
| 第三层 | 浏览器 CDP | 完整浏览器自动化 |

优先使用轻量方式，逐步升级，节省 token 和时间。

## 核心功能

- **复用 Chrome 登录态**：直接连接用户日常 Chrome，自然继承已有登录状态
- **完整浏览器控制**：打开页面、执行 JS、点击元素、截图、视频控制
- **并行分治**：多个子 Agent 共享同一 Chrome 实例，不同 targetId 在不同标签页运行
- **站点经验累积**：`references/site-patterns/` 存储各网站操作经验，持续优化

## 设置

Chrome 地址栏 → `chrome://inspect/#remote-debugging` → 勾选允许远程调试

## Skill vs MCP

Skill 不仅提供工具，还提供工具 + 策略 + 经验的完整方案。

## 应用场景

- 需登录网站的广泛调研（如小红书旅游体验）
- 社媒自动化填写草稿
- 多 Agent 并行竞品调研
- 同时操作 100+ 浏览器网页

## 为什么值得关注

三层通道调度是智能 Agent 设计的典范——渐进式升级策略优化成本和性能。直接使用已登录浏览器大幅降低使用门槛，在 Claude Code 生态中提供了比官方工具更强大的网络能力。

## 相关链接

- GitHub: https://github.com/eze-is/web-access
