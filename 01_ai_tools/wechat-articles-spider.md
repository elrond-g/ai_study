# wechat_articles_spider

> klin-h | Python + Selenium | https://github.com/klin-h/wechat_articles_spider

## 项目简介

轻量级微信公众号文章爬虫，核心优势是不依赖数据包捕获工具，相比其他方案更稳定和易于部署。支持近期文章、历史全量和关键词搜索三种模式。

## 三种爬取模式

| 模式 | 说明 |
|------|------|
| 近期文章 | 抓取过去两天内更新的文章 |
| 历史全量 | 获取指定公众号所有历史文章 |
| 关键词搜索 | 自定义关键词 + 权重评分排序筛选 |

## 核心特点

- 无需数据包捕获（Fiddler/Charles 等），降低技术门槛
- 从 Excel 批量读取公众号列表
- 输出结构化 Excel（公众号名、标题、链接、发布时间）
- Selenium + Chrome 自动化驱动

## 技术栈

- Selenium（浏览器自动化）
- webdriver-manager（驱动版本管理）
- Pandas（数据处理和输出）
- wechatarticles（微信文章获取库）

## 注意事项

- 需预先注册微信公众号账号（建议用新号）
- 受 WeChat 频率限制和反爬虫机制约束
- 需遵守相关法律法规

## 相关链接

- GitHub: https://github.com/klin-h/wechat_articles_spider
