# claude-plugin-weixin

> ⭐ 517 | TypeScript | https://github.com/m1heng/claude-plugin-weixin

## 项目简介

Claude Code 的微信频道插件，让开发者可以在终端中直接接收和回复微信消息。基于腾讯官方 iLink Bot API（微信 ClawBot 插件功能），使用 HTTP 长轮询，无需公网 IP 或 Webhook 配置。

## 核心功能

- **微信消息接收**：在 Claude Code 终端中实时接收微信消息
- **消息回复**：通过终端直接发送微信回复
- **无公网依赖**：HTTP 长轮询模式，内网即可运行
- **Claude Code 插件**：通过 `claude plugin` 命令一键安装

## 安装方式

```bash
# 添加插件市场
claude plugin marketplace add m1heng/claude-plugins

# 安装插件
claude plugin install weixin
```

## 技术特点

- 基于腾讯官方 iLink Bot API（`ilinkai.weixin.qq.com`），非灰色方案
- Bun 运行时，轻量快速
- HTTP 长轮询，无需公网 IP 和 ngrok

## 与其他方案的区别

不同于逆向 iPad 协议的灰色方案，本插件基于腾讯 2026 年正式开放的微信 ClawBot 官方 API，合规且稳定。

## 相关链接

- GitHub: https://github.com/m1heng/claude-plugin-weixin
