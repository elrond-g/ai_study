# weixin-agent-sdk

> ⭐ 812 | TypeScript | https://github.com/wong2/weixin-agent-sdk

## 项目简介

微信 AI Agent 桥接框架，通过 ACP（Agent Client Protocol）协议，将 Claude Code、Codex、kimi-cli 等任意 AI Agent 接入微信。代码改造自腾讯官方 `@tencent-weixin/openclaw-weixin` 包，仅供学习使用。

## 核心功能

- **ACP 协议适配**：实现 Agent Client Protocol，让 AI Agent 以标准化方式接入微信
- **多 Agent 支持**：Claude Code、Codex、kimi-cli 等均可通过同一 SDK 接入
- **SDK 分包**：`weixin-agent-sdk`（桥接核心）+ `agent-acp`（ACP 适配器）

## 项目结构

```
packages/
  sdk/              微信桥接 SDK（核心）
  agent-acp/        ACP 协议适配器
  example-openai/   基于 OpenAI 的使用示例
```

## ACP 协议说明

ACP（Agent Client Protocol）是一套开放的 Agent 接入协议，定义了 Agent 与客户端之间的标准通信方式，使不同 AI Agent 可以透明接入各类 IM 平台。

## 使用场景

- 将 Claude Code 或其他 AI Agent 接入微信个人账号
- 基于 ACP 协议构建多平台 Agent 桥接方案
- 学习 AI Agent 与 IM 平台的集成架构

## 相关链接

- GitHub: https://github.com/wong2/weixin-agent-sdk
