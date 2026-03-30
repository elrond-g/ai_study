# XCrawl

> API 服务 | https://www.xcrawl.com | https://docs.xcrawl.com

## 项目简介

XCrawl 是 AI 就绪的网页数据提取 API，专为 AI Agent 和 LLM 工作流设计。将任何网站转为结构化 JSON/Markdown/HTML 数据，内置代理轮转和反爬虫突破。原生支持 MCP 协议和 OpenClaw 集成。

## 核心功能

- **多输出格式**：JSON（系统集成）、Markdown（LLM 友好）、HTML、截图
- **动态内容处理**：SPA、无限滚动、客户端渲染
- **反爬虫突破**：高级浏览器指纹 + 轮转住宅代理
- **LLM 优化**：Markdown 输出降低 Token 消耗
- **RAG 友好**：清洁数据直接用于 RAG 管道和微调数据集

## API 端点

| 端点 | 用途 |
|------|------|
| Scrape API | 单页数据提取 |
| Search API | 搜索引擎结果 |
| Map API | 站点地图发现 |
| Crawl API | 多页批量爬取 |

## OpenClaw 集成

通过 MCP 协议使 AI Agent 直接调用网页爬取功能。实时网页访问 + 结构化数据输出，Agent 可进行研究、验证和监控。

## SDK 支持

Python、Node.js/TypeScript（官方），Go、Ruby、PHP（社区）。支持 n8n 和 Zapier 无代码集成。

## 定价

1000 个免费额度，支持从数千到数百万级日请求量。

## 为什么值得关注

相比传统爬虫依赖 CSS 选择器和 XPath，XCrawl 的 AI 能自适应网站变化，维护成本降低 90%。MCP 原生支持使 AI Agent 获得实时网络信息访问能力。

## 相关链接

- 官网: https://www.xcrawl.com
- 文档: https://docs.xcrawl.com
- OpenClaw 集成: https://docs.xcrawl.com/zh/doc/developer-guides/openclaw/
