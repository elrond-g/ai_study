# cc-weixin

> ⭐ 86 | TypeScript | https://github.com/hao-ji-xing/cc-weixin

## 项目简介

基于腾讯官方 iLink Bot API（微信 ClawBot 插件功能），在微信里直接使用 Claude Code Agent。这是一个早期 demo 项目，标志着微信首次合法开放个人 Bot API 这一历史性时刻。

## 背景：微信首次开放个人 Bot API

2026 年，腾讯通过 OpenClaw（AI Gateway）正式开放微信个人账号的 Bot API，底层协议为 **iLink**（智联），接入域名 `ilinkai.weixin.qq.com`。

| 接入方式 | 典型实现 | 性质 |
|------|------|------|
| 逆向 iPad 协议 | WeChatPadPro、itchat | 灰色地带，违反协议 |
| PC 客户端 Hook | 注入 DLL | 灰色地带 |
| iLink 官方 API | cc-weixin、weclaw 等 | **官方合规** |

## 核心功能

- **微信接入 Claude Code**：在微信对话中直接向 Claude Code Agent 发指令
- **官方 API**：基于 iLink 官方协议，账号安全有保障
- **demo 级实现**：展示核心接入逻辑，适合作为学习和二次开发基础

## 相关链接

- GitHub: https://github.com/hao-ji-xing/cc-weixin
- OpenClaw 文档: https://docs.openclaw.ai
