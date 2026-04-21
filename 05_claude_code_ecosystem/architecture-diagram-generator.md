# Architecture Diagram Generator

> ⭐ 3.9k | MIT | https://github.com/Cocoon-AI/architecture-diagram-generator

## 项目简介

Claude Skill，用自然语言生成专业级系统架构图，输出为暗色主题的独立 HTML 文件，无需专门设计软件或 Mermaid 语法。通过 Claude 聊天实时迭代优化图表。

## 核心特性

- **独立 HTML 输出**：单文件包含 SVG + CSS，无外部依赖
- **暗色主题**：统一视觉风格，组件按语义色彩编码
- **对话式迭代**：直接在 Claude 聊天窗口反复修改
- **JetBrains Mono 字体**：技术图表专业感
- **自包含 SVG**：可直接嵌入文档或分享

## 使用要求

- Claude Pro / Max / Team / Enterprise 订阅
- 作为 Claude Code Skill 安装

## 使用方式

用户以自然语言描述架构（如"微服务 + Redis 缓存 + PostgreSQL + Kafka 消息队列"），Claude 返回可渲染的 HTML 架构图，可通过对话微调组件、连线、颜色等。

## 使用场景

- 技术方案文档配图
- 系统设计评审
- 快速原型架构说明
- 非设计背景的工程师快速产出专业图表

## 相关链接

- GitHub: https://github.com/Cocoon-AI/architecture-diagram-generator
