# Larksuite CLI（飞书 CLI）

> ⭐ 1.9k+ | Go + Node.js | https://github.com/larksuite/cli | MIT

## 项目简介

飞书/Lark 官方命令行工具，为人类用户和 AI Agent 双场景设计。覆盖消息、文档、表格、日历、邮件、任务、会议等核心业务域，提供 200+ 命令和 19 个 AI Agent 技能。

## 三层命令架构

| 层级 | 说明 |
|------|------|
| 快捷命令（`+` 前缀） | 人类和 AI 友好，内置智能默认值 |
| API 命令 | 从飞书 OAPI 元数据自动生成 |
| 原始 API 调用 | 覆盖 2500+ 开放平台 API 端点 |

## 支持的业务域（11 个）

即时通讯、文档、表格、数据库、日历、邮件、任务、会议（含会议记录和录音）、用户管理、文件操作

## AI Agent 集成

- **19 个结构化技能**：开箱即用，兼容主流 AI 工具
- **Claude Code 一键安装**：`npx skills add larksuite/cli -y -g`
- **Dry-run 预览**：执行前可预览操作结果
- **表格输出**：结构化数据便于 Agent 解析

## 安装

```bash
npm install -g @larksuite/cli
```

## 为什么值得关注

1. **AI 原生设计**：19 个预定义技能可直接用于 LLM 应用
2. **2500+ API 覆盖**：飞书全量功能命令行化
3. **字节跳动官方**：Lark Technologies 维护，持续更新
4. **三层架构**：初学者用快捷命令，高级用户用原始 API，灵活适配

## 相关链接

- GitHub: https://github.com/larksuite/cli
- 开发者文档: https://open.larksuite.com/
