# OpenTwitter MCP

> 6551Team | Python (FastMCP) | https://clawhub.ai/infra403/opentwitter-mcp | https://github.com/6551Team/opentwitter-mcp

## 项目简介

OpenTwitter MCP 是通过 6551 REST API 为 AI Agent 提供 Twitter/X 数据访问的 MCP 服务器。支持用户资料查询、推文搜索、粉丝事件监测和 KOL 追踪。

## 核心功能

- **数据检索**：用户资料、推文搜索、用户推文列表
- **特殊能力**：访问已删除推文
- **实时监测**：粉丝增减事件（新增/取消关注）
- **KOL 追踪**：监控关键意见领袖的关注者动态
- **社媒管理**：发布推文、管理列表、书签、群聊

## 使用方式

1. 在 https://6551.io/mcp 获取 API Token
2. 配置 `TWITTER_TOKEN` 环境变量
3. 在 Claude Desktop/Claude Code 中集成

## 技术架构

基于 FastMCP 框架，8 个工具 + 配置加载器。依赖 mcp (>=1.25) 和 httpx (>=0.27)。

## 为什么值得关注

使 AI Agent 能直接与 Twitter/X 互动，KOL 追踪和实时事件监测对社交媒体分析和影响力营销有重要价值。与 ClawHub 生态集成。

## 相关链接

- ClawHub: https://clawhub.ai/infra403/opentwitter-mcp
- GitHub: https://github.com/6551Team/opentwitter-mcp
