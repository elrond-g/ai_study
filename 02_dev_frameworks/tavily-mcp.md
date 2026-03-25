# Tavily MCP

> ⭐ N/A | TypeScript | https://github.com/tavily-ai/tavily-mcp

## 项目简介

专为 AI Agent 设计的搜索引擎 MCP Server，返回结构化的搜索结果数据，一分钟即可接入，让 LLM 获得实时联网搜索能力。

## 核心功能

- **结构化搜索结果**：返回清洗后的结构化数据，直接可供 LLM 消费，无需额外解析
- **MCP 协议接入**：遵循 Model Context Protocol 标准，与 Claude 等支持 MCP 的客户端无缝集成
- **快速部署**：简单配置 API Key 即可启动，一分钟完成接入

## 技术特点

- 搜索结果经过去噪和摘要处理，token 消耗更低
- 支持搜索深度和主题等参数自定义
- 专门针对 AI Agent 场景优化，比通用搜索 API 更适合 LLM 调用

## 使用场景

- 为 Claude Code 等 AI 工具添加实时网络搜索能力
- Agent 在执行任务时自主搜索最新信息辅助决策
- 构建需要实时数据的 RAG 应用

## 相关链接

- GitHub: https://github.com/tavily-ai/tavily-mcp
