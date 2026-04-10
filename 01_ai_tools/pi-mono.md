# Pi Mono (pi-coding-agent)

> ⭐ 33,800+ | TypeScript | https://github.com/badlogic/pi-mono

## 项目简介

Pi Mono 是 Mario Zechner（badlogic，libGDX 作者）开发的 AI Agent 工具包 monorepo，核心产品 pi-coding-agent 是一个交互式编码 Agent CLI。整个 monorepo 包含 7 个子包，覆盖统一 LLM API、Agent 运行时、终端 UI、Web UI、Slack Bot 和 vLLM 部署管理。

## 子包一览

| 包名 | 描述 |
|------|------|
| **@mariozechner/pi-ai** | 统一多提供商 LLM API（OpenAI、Anthropic、Google 等） |
| **@mariozechner/pi-agent-core** | Agent 运行时，工具调用与状态管理 |
| **@mariozechner/pi-coding-agent** | 交互式编码 Agent CLI（核心产品） |
| **@mariozechner/pi-mom** | Slack Bot，将消息委托给 pi coding agent |
| **@mariozechner/pi-tui** | 终端 UI 库，差分渲染 |
| **@mariozechner/pi-web-ui** | AI 聊天界面 Web 组件 |
| **@mariozechner/pi-pods** | vLLM GPU Pod 部署管理 CLI |

## 核心功能

- **编码 Agent CLI**：交互式终端编码 Agent，支持工具调用和状态管理
- **统一 LLM API**：一套接口调用 OpenAI、Anthropic、Google 等多家模型
- **Agent 运行时**：内置工具调用和状态管理的 Agent 核心框架
- **TUI/Web UI 库**：终端差分渲染 UI 和 Web 聊天组件，可复用于其他项目
- **vLLM 部署**：GPU Pod 上管理 vLLM 推理服务的 CLI 工具
- **Slack 集成**：通过 Slack Bot 将消息转发给编码 Agent

## 技术特点

- TypeScript monorepo 架构
- MIT 许可证
- 鼓励公开分享 OSS 编码 Agent 会话数据，改进编码 Agent 质量
- 支持 Hugging Face 数据集发布会话记录

## 使用场景

- AI 辅助编程和代码生成
- 构建自定义 AI Agent 的基础设施
- 统一管理多 LLM 提供商接入
- vLLM 模型部署与管理
- 为其他项目提供 TUI/Web UI 组件

## 相关链接

- GitHub: https://github.com/badlogic/pi-mono
- 官网: https://pi.dev
- Discord 社区: https://discord.com/invite/3cU7Bz4UPx
