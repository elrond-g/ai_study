# OpenHuman

> ⭐ 开源 | TypeScript + Rust | https://github.com/tinyhumansai/openhuman

## 项目简介

OpenHuman 是一个开源的 AI Agent 个人助手桌面应用，以人为中心设计，提供简洁的 UI 体验、持久记忆和 118+ 第三方集成。不同于终端优先的 Agent 工具，OpenHuman 提供桌面 UI 和宠物化吉祥物交互，几分钟内即可完成从安装到可用的全流程。

## 核心特性

### 118+ 第三方集成 + 自动同步
通过一键 OAuth 接入 Gmail、Notion、GitHub、Slack、Stripe、Calendar、Drive、Linear、Jira 等 118+ 服务。每 20 分钟自动拉取活跃连接的最新数据到 Memory Tree，Agent 无需等待即可掌握最新上下文。

### Memory Tree + Obsidian Wiki
本地优先的知识库，所有接入数据被标准化为 ≤3K Token 的 Markdown 块，分层汇总存储在本地 SQLite 中。同时生成 Obsidian 兼容的 `.md` 文件库，受 Karpathy 的 obsidian-wiki 工作流启发。

### TokenJuice 智能压缩
每次工具调用、爬取结果、邮件正文和搜索内容都会经过 Token 压缩层处理后再发给 LLM。HTML → Markdown、长 URL 缩短、冗余输出去重和摘要，最多减少 80% Token 消耗和延迟。

### 内置工具集
Web 搜索、爬虫、完整编码工具集（文件系统/git/lint/test/grep）、原生语音（STT 输入 + ElevenLabs TTS 输出 + 吉祥物口型同步 + Google Meet 实时 Agent）。模型路由自动将任务分发给合适的 LLM（推理/快速/视觉）。

### 消息通道
支持通过用户已有的消息渠道（Telegram/Discord 等）进行入站和出站通信，工作流数据本地加密存储。

## 技术架构

- 前端：桌面应用（Tauri + CEF）
- 后端代理层：Composio 集成连接器（可选直连模式）
- 本地存储：SQLite + Obsidian 兼容 Markdown 文件库
- 可选集成：agentmemory 后端、Ollama 本地 AI
- 开发依赖：Node.js 24+、pnpm 10.10.0、Rust 1.93.0、CMake、Ninja

## 与其他 Agent 框架对比

- vs Claude Cowork：开源、更多集成、本地数据存储
- vs OpenClaw：UI 优先而非终端优先、OAuth 一键集成、自动同步
- vs Hermes Agent：零配置启动、桌面体验、内置记忆树

## GitHub

https://github.com/tinyhumansai/openhuman
