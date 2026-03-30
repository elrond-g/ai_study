# Tentix

> Labring | TypeScript (Bun + Hono) | https://github.com/labring/tentix

## 项目简介

Tentix（TenTix，10x 效率）是 Labring 开发的 AI 原生客户服务平台，目标是实现 10 倍更快响应、10 倍更少人工干预、10 倍更高用户满意度。基于 FastGPT 构建，集前端、后端 API 和 AI 处理于一体。

## 核心功能

- **AI 智能客服**：基于 FastGPT 的智能对话，理解用户意图并准确响应
- **多渠道集成**：统一管理飞书、微信等多平台客户咨询
- **工单全生命周期**：创建 → 分配 → 处理 → 解决 → 归档
- **人机无缝切换**：AI 自动回复 + 必要时无缝转人工
- **AI 知识库**：文档处理和 RAG 检索增强
- **MCP 扩展**：支持 Model Context Protocol 扩展 AI 能力

## 技术栈

| 组件 | 技术 |
|------|------|
| 运行时 | Bun |
| Web 框架 | Hono 4.7 |
| 数据库 | PostgreSQL + Drizzle ORM |
| Monorepo | Turborepo |
| 对象存储 | MinIO (S3 兼容) |
| API 文档 | OpenAPI + Scalar |

## 为什么值得关注

1. **Labring 生态**：与 Sealos、FastGPT 紧密集成，云原生部署
2. **AI 原生设计**：从架构层面原生支持 AI，非后期集成
3. **现代技术栈**：Bun + Hono + Turborepo，开发和构建极速
4. **开源可控**：完整的全栈解决方案，支持私有化部署

## 相关链接

- GitHub: https://github.com/labring/tentix
- FastGPT: https://github.com/labring/FastGPT
