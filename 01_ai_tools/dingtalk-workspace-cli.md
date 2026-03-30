# DingTalk Workspace CLI

> 钉钉官方 | Apache-2.0 | https://github.com/DingTalk-Real-AI/dingtalk-workspace-cli

## 项目简介

钉钉官方开源的跨平台命令行工具，将钉钉全套产品能力统一集成到 CLI 中，专为 AI Agent 和人类用户双场景设计。Agent 可直接调用数千个钉钉能力，无需 GUI 模拟点击。

## 十大产品能力

AI 表格、日历、日志、待办事项、机器人、通讯录、钉一下消息、考勤、开放平台文档、工作区

## AI Agent 集成

- 结构化 JSON 响应输出，开箱即用的 Agent Skills
- Skills 采用 SKILL.md 格式（纯提示词描述，无代码执行风险）
- 原生支持 Claude Code、Cursor 等主流 AI 编码环境
- Agent 直接通过 CLI 调用钉钉 API，跳过 GUI

## 安全架构（零信任）

- **认证**：OAuth device-flow + 域名白名单 + 最小权限
- **加密**：PBKDF2 + AES-256-GCM，以设备 MAC 地址为密钥
- **凭证隔离**：跨平台 Keychain/DPAPI，令牌无法在其他设备解密
- **审计**：每个 API 调用必须通过钉钉开放平台认证和审计链
- **域名限制**：Bearer 令牌仅发送到 `*.dingtalk.com`

## 安装

```bash
curl -fsSL https://raw.githubusercontent.com/DingTalk-Real-AI/dingtalk-workspace-cli/main/scripts/install.sh | sh
```

## 为什么值得关注

1. **首个 AI-Native 企业办公 CLI**：针对 AI Agent 场景深度优化，而非事后适配
2. **零信任安全**：设备绑定加密 + 完整审计链，企业级安全
3. **钉钉官方维护**：阿里旗下，与悟空 Agent 平台深度集成

## 相关链接

- GitHub: https://github.com/DingTalk-Real-AI/dingtalk-workspace-cli
