# OpenNews MCP

> 6551Team | Python | https://clawhub.ai/infra403/opennews-mcp | https://github.com/6551Team/opennews-mcp

## 项目简介

OpenNews MCP 是专业加密货币新闻聚合 MCP 服务器，整合 72+ 实时数据源的加密市场新闻，通过 AI 驱动的情感分析和交易信号为 Claude 等 AI 助手提供实时市场情报。

## 核心功能

- **新闻聚合**：72+ 实时数据源（Bloomberg、Reuters、CoinDesk、Cointelegraph、The Block 等）
- **AI 评分**：情感分析 + 评级（评分、等级、看涨/看跌信号）
- **交易信号**：基于新闻内容生成方向指引
- **实时推送**：WebSocket 端点 `wss://ai.6551.io/open/news_wss`
- **双语摘要**：中英文摘要

## 使用方式

1. 在 https://6551.io/mcp 获取 API Token
2. 配置环境变量 `OPENNEWS_TOKEN`
3. 在 Claude Desktop 或其他 MCP 客户端中集成

## 技术栈

Python，依赖 mcp、httpx、websockets。支持 Claude Desktop、VS Code with Cline 等 MCP 兼容平台。

## 为什么值得关注

72+ 数据源的全面覆盖 + AI 情感评分为加密交易者提供了一站式市场情报。WebSocket 实时推送保证决策时效性。

## 相关链接

- ClawHub: https://clawhub.ai/infra403/opennews-mcp
- GitHub: https://github.com/6551Team/opennews-mcp
