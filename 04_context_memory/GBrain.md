# GBrain

> Gist | Garry Tan | https://gist.github.com/garrytan/49c88e83cf8d7ae95e087426368809cb

## 项目简介

GBrain 是 YC CEO Garry Tan 发布的开源个人知识大脑设计文档，基于 SQLite + FTS5 + 向量嵌入的单文件知识库方案，MCP-ready，作为 GStack 的知识层设计蓝图。

## 核心设计

- **单文件知识库**：基于 SQLite 的轻量存储方案
- **全文搜索**：FTS5 引擎支持高效文本检索
- **向量嵌入**：支持语义搜索和相似度匹配
- **MCP Ready**：原生适配 MCP 协议，可接入 AI Agent

## 技术特点

- SQLite + FTS5 + 向量嵌入三位一体
- 单文件部署，零外部依赖
- 为 GStack 多 Agent 系统提供持久化知识层

## 使用场景

- 个人知识管理系统设计参考
- AI Agent 长期记忆的轻量实现方案
- MCP 服务的知识存储后端

## 相关链接

- Gist: https://gist.github.com/garrytan/49c88e83cf8d7ae95e087426368809cb
- GStack: https://github.com/garrytan/gstack
