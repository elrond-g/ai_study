# MediaCrawler

> ⭐ 15,000+ | Python + Playwright | https://github.com/NanmiCoder/MediaCrawler

## 项目简介

MediaCrawler 是开源的多平台自媒体数据采集工具，提供用户友好的爬虫框架，支持七大中文社交平台的公开信息采集。曾登上 GitHub Trending，被誉为"开源爆款工具"。

## 支持的 7 个平台

| 平台 | 采集内容 |
|------|----------|
| 小红书 | 笔记、评论 |
| 抖音 | 视频、评论 |
| 快手 | 视频、评论 |
| B 站 | 视频、评论 |
| 微博 | 帖子、评论 |
| 百度贴吧 | 帖子、评论、回复 |
| 知乎 | 问答文章、评论 |

## 核心功能

- **灵活登录**：二维码登录 + Cookie 登录，登录状态缓存
- **采集方式**：关键词搜索 + ID 直接采集，一级和二级评论
- **多种存储**：CSV、JSON、JSONL、Excel、SQLite、MySQL
- **Web 界面**：可视化操作界面，无需命令行
- **词云生成**：评论词云便于数据分析
- **反爬处理**：自动代理和验证码处理

## 技术栈

- Playwright 浏览器自动化
- Node.js + uv（Python 包管理）
- API 服务器（默认 8080 端口）+ WebUI
- 基于保存登录状态 + JS 表达式获取签名，无需复杂 JS 逆向

## 为什么值得关注

一个工具覆盖七大中文社交平台，Web 界面大幅降低使用门槛。15K+ Stars 反映了对中文社交媒体数据采集工具的强烈需求。

## 注意事项

项目强调作为技术研究和学习工具，用户需遵守《网络安全法》等相关法律法规。

## 相关链接

- GitHub: https://github.com/NanmiCoder/MediaCrawler
- 文档: https://nanmicoder.github.io/MediaCrawler/
