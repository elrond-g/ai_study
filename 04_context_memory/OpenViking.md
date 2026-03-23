# OpenViking

> ⭐ 18,269 | Python | https://github.com/volcengine/OpenViking | https://openviking.ai

## 项目简介

OpenViking 是字节跳动（火山引擎）开源的 AI Agent 专用上下文数据库，通过文件系统范式统一管理 Agent 所需的三类上下文：记忆（Memory）、资源（Resources）和技能（Skills）。支持分层上下文传递和自进化能力，专为 OpenClaw、Claude Code 等编程 Agent 设计。

## 核心功能

- **三类上下文统一管理**：记忆（对话历史）、资源（文件/工具）、技能（Skills）一体化
- **文件系统范式**：用熟悉的目录/文件结构组织上下文，直观可操作
- **分层上下文传递**：支持全局、项目、会话三个层级的上下文继承
- **自进化**：Agent 可以自动更新和扩充自己的上下文数据库
- **Agentic RAG**：针对 Agent 场景优化的检索增强生成

## 技术特点

- Python 实现，与 OpenClaw/Claude Code 深度集成
- 支持 MCP 协议，作为 Context 工具服务器
- 结构化存储，支持语义检索

## 使用场景

- 为 Claude Code 等 Agent 提供持久化的项目知识库
- 构建跨会话保持连贯性的长期 AI 助手
- Agent 自主积累和管理工作记忆

## 相关链接

- GitHub: https://github.com/volcengine/OpenViking
- 官网: https://openviking.ai
