# GBrain

> ⭐ 9.6k | TypeScript | MIT | https://github.com/garrytan/gbrain

## 项目简介

Garry Tan（YC 总裁）出品的开源 AI Agent 知识大脑实现。从最初的单文件设计 Gist 演化为完整的 Knowledge Management System，提供持久化记忆、结构化信息检索和自主任务执行，服务于 OpenClaw / Hermes 等 Agent 生态。

## 核心特性

- **混合检索**：向量 + 关键词 + 图遍历三路召回
- **自动关联知识图谱**：带类型化关系的实体链接
- **26 个运维 Skills**：数据摄取、信息富化、维护清理
- **Minions 任务队列**：确定性后台作业执行
- **语音集成**：支持语音输入与多源数据采集
- **MCP Server**：Claude 等 Agent 直接调用

## 检索性能

- **95% Recall@5**（vs 基线 83%）
- 层级检索策略：Embedding + FTS + 图遍历组合
- 支持自然语言查询与结构化查询

## 技术栈

- **语言**：TypeScript
- **存储**：PostgreSQL（含 pgvector）或 PGLite
- **平台**：Supabase 兼容
- **接入**：MCP 协议原生支持

## 使用场景

- GStack 多 Agent 系统的持久化知识层
- 个人/团队 AI 知识管理中台
- 需要高召回率的 Agent Retrieval 场景

## 相关链接

- GitHub: https://github.com/garrytan/gbrain
- 原始设计 Gist: https://gist.github.com/garrytan/49c88e83cf8d7ae95e087426368809cb
- GStack: https://github.com/garrytan/gstack
