# weclaw

> ⭐ 548 | Go | https://github.com/fastclaw-ai/weclaw

## 项目简介

通过微信 ClawBot 将任意 AI Agent 接入微信的桥接服务。基于腾讯官方 iLink 协议，由 fastclaw-ai 开发，是微信 AI Agent 生态中最轻量的 Go 实现之一。

## 核心功能

- **任意 Agent 接入**：不限于 Claude Code，任意遵循 ACP 或标准接口的 Agent 均可接入
- **微信 ClawBot**：通过腾讯官方 ClawBot 插件框架，合规接入微信
- **Go 实现**：高性能、低资源占用，适合长期运行的桥接服务
- **简单部署**：单二进制文件，Docker 友好

## 在微信 AI Agent 生态中的位置

```
微信用户
   ↓ 发消息
微信 ClawBot（官方 iLink API）
   ↓
weclaw（本项目，Go 桥接层）
   ↓
任意 AI Agent（Claude Code / Codex / 自定义 Agent）
```

## 与同类项目对比

| 项目 | 语言 | 特点 |
|------|------|------|
| weclaw | Go | 轻量，单二进制，任意 Agent |
| weixin-bot | Python/Node | 零配置，双语言 |
| cc-weixin | TypeScript | Claude Code 专用，demo 级 |

## 相关链接

- GitHub: https://github.com/fastclaw-ai/weclaw
