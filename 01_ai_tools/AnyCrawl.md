# AnyCrawl

> ⭐ 3.1K+ | TypeScript / Node.js | https://github.com/any4ai/AnyCrawl | https://anycrawl.dev

## 项目简介

AnyCrawl 是高性能爬取与抓取工具包，将网站转为 LLM 友好数据，并从 Google/Bing/Baidu 等搜索引擎提取结构化 SERP 结果，原生多线程 / 多进程批处理。

## 核心功能

- **Scrape / Crawl / SERP 三合一**：单页抓取、整站爬取、多搜索引擎结果聚合统一 API
- **三引擎可选**：`cheerio`（静态 HTML 最快）、`playwright`、`puppeteer`（动态 JS 渲染）
- **LLM 结构化提取**：通过 JSON Schema 声明目标字段，自动从页面抽取结构化数据

## 技术特点

- Node.js / TypeScript + Redis，多线程多进程处理批量任务
- 内置缓存控制（`max_age` / `store_in_cache`）、代理支持（HTTP/SOCKS）
- 支持自托管 Docker Compose 部署，API Key 认证

## 使用场景

- RAG 系统的大规模网页数据采集管道
- AI Agent 实时搜索（替代 Google 付费 API）
- 站点全量索引构建与内容更新监控

## 相关链接

- GitHub: https://github.com/any4ai/AnyCrawl
- 官网: https://anycrawl.dev
- 文档: https://docs.anycrawl.dev
