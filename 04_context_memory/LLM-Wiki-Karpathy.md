# LLM Wiki（Karpathy）

> Gist | Andrej Karpathy | https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

## 项目简介

Karpathy 提出的 LLM Wiki 模式：让 LLM 增量构建并维护持久化个人知识 Wiki，替代传统 RAG 实现知识复利积累。核心思路是让 AI 在每次对话中将有价值的信息沉淀到一个持久化的 Wiki 中，配合 Obsidian 等工具使用。

## 核心理念

- **知识复利**：每次对话都为知识库增值，而非一次性消费
- **替代 RAG**：用增量写入的 Wiki 替代检索增强生成的被动模式
- **持久化积累**：跨会话的知识持续沉淀和关联
- **配合 Obsidian**：利用 Obsidian 的双向链接和图谱特性

## 技术特点

- 增量式知识构建，非检索式被动获取
- 与笔记工具深度集成
- LLM 自主判断知识价值和关联

## 使用场景

- 个人知识管理的新范式探索
- AI Agent 长期记忆架构设计参考
- 替代 RAG 的知识积累方案

## 相关链接

- Gist: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
