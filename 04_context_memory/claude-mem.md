# claude-mem

> https://github.com/thedotmack/claude-mem

## 项目简介

claude-mem 是专为 Claude AI 设计的记忆插件，通过持久化存储为 Claude 提供跨会话的长期记忆能力。Claude 本身不记住上一次对话的内容，claude-mem 通过在每次对话时自动注入历史记忆来弥补这一限制。

## 核心功能

- **自动记忆注入**：每次对话开始时自动将相关历史记忆加载到 Claude 的上下文中
- **记忆提取**：从对话中自动识别和提取值得记住的信息
- **记忆检索**：按相关性检索最适合当前对话的历史记忆
- **手动管理**：支持查看、编辑、删除已保存的记忆

## 技术特点

- 与 Claude API 集成，透明度高
- 本地存储或可配置的后端存储
- 基于语义相似度的记忆召回

## 使用场景

- 构建"记得住你"的个人 Claude 助手
- 在长期项目中保持 AI 对上下文的连贯理解
- 减少每次对话重新解释背景信息的成本

## 相关链接

- GitHub: https://github.com/thedotmack/claude-mem
