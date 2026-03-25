# Context7

> ⭐ N/A | TypeScript | https://github.com/upstash/context7

## 项目简介

将最新库文档注入 LLM 上下文的 MCP Server，在 prompt 中加上 "use context7" 即可让 AI 获取目标库的最新官方文档，告别过时 API 幻觉。

## 核心功能

- **实时文档注入**：自动拉取目标库的最新文档并注入上下文，确保 LLM 生成的代码基于最新 API
- **极简触发方式**：只需在 prompt 中添加 "use context7" 即可激活，零学习成本
- **广泛库覆盖**：支持主流编程语言和框架的文档索引

## 技术特点

- 基于 MCP 协议，与 Claude Code 等工具原生集成
- 文档经过预处理和分块，高效利用上下文窗口
- 自动匹配 prompt 中提到的库名并检索对应文档

## 使用场景

- 使用 Claude Code 开发时获取依赖库的最新 API 文档
- 避免 LLM 因训练数据过时而生成已废弃的 API 调用
- 学习新框架时让 AI 基于最新文档回答问题

## 相关链接

- GitHub: https://github.com/upstash/context7
