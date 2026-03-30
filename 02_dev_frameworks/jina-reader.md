# Jina Reader (r.jina.ai)

> Jina AI | API 服务 | https://r.jina.ai | https://github.com/jina-ai/reader

## 项目简介

Jina Reader 是一个 URL 转 LLM 友好格式的 API 服务。在目标 URL 前加 `https://r.jina.ai/` 前缀，即可将任何网页转为干净的 Markdown 或 JSON，专为大语言模型优化。

## 使用方式

```
https://r.jina.ai/https://example.com
```

就这么简单。

## 核心功能

- **网页转 Markdown**：自动提取主要内容，去除广告和噪声
- **PDF 支持**：原生读取和转换 PDF
- **图像描述**：自动为网页图片生成描述标注
- **JS 渲染**：Puppeteer + 无头 Chrome，支持动态网站
- **结构化提取**：ReaderLM-v2 模型支持 JSON Schema 提取
- **搜索端点**：`s.jina.ai` 执行网络搜索返回前 5 个 LLM 友好结果

## 定价

| 层级 | RPM | TPM | 并发 |
|------|-----|-----|------|
| 免费 | 100 | 100K | 2 |
| 付费 | 500 | 200 万 | 50 |
| 高级 | 5,000 | 5000 万 | 500 |

新 API 密钥含 1000 万免费 Token，约 $0.02/百万 Token。

## 技术特点

- 通常 2 秒内返回结果
- 支持 `x-wait-for-selector` 等待特定元素渲染
- 开源（GitHub 可用）
- 集成 Airbyte、Haystack 等框架

## 为什么值得关注

LLM 时代的"网页翻译器"——将混乱的网页转为模型可直接消费的干净数据。零配置的 URL 前缀方式极其简洁，免费层足够原型和测试，是 RAG 管道和 Agent 联网的基础设施。

## 相关链接

- 服务: https://r.jina.ai
- GitHub: https://github.com/jina-ai/reader
- API 文档: https://jina.ai/reader/
