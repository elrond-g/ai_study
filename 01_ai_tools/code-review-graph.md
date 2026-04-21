# code-review-graph

> ⭐ 11.8k | MIT | https://github.com/tirth8205/code-review-graph

## 项目简介

本地运行的代码知识图谱工具，专为降低 AI Code Review 的 Token 消耗设计。通过 Tree-sitter 解析代码仓库结构，提供"影响半径分析"和上下文检索，替代 AI Agent 每次重读整个仓库。

## 核心特性

- **Blast-radius 分析**：变更函数→受影响文件/函数的依赖链路
- **增量更新**：<2 秒完成变更索引
- **23+ 语言支持**：覆盖主流编程语言 + Jupyter Notebook
- **MCP 集成**：28 个 MCP 工具暴露给 AI Assistant
- **社区检测**：识别代码库的模块化结构
- **多仓注册表**：同时管理多个代码库
- **语义搜索**：基于 sentence-transformers 的嵌入式检索

## 性能数据

- **平均 Token 减少 8.2 倍**
- **Monorepo 场景最高 49 倍** Token 压缩
- 单次分析可替代数次全仓库 read

## 技术栈

- Python + Tree-sitter（语法解析）
- SQLite（图存储）
- MCP 协议（AI 工具集成）
- sentence-transformers（向量嵌入）

## 使用场景

- AI 辅助代码审查（PR Review）
- 大型 Monorepo 的结构化理解
- Claude Code / Cursor / Codex 的上下文优化
- 重构影响范围预估

## 相关链接

- GitHub: https://github.com/tirth8205/code-review-graph
