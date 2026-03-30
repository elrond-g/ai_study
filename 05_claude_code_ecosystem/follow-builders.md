# follow-builders

> Zara Zhang | Claude Skill + Node.js | https://github.com/zarazhangrui/follow-builders

## 项目简介

follow-builders 是一个 AI 构建者内容聚合 Skill，核心理念"Follow builders, not influencers"——关注真正在构建产品的人。自动监控 25+ 顶尖 AI 构建者在 X/Twitter、播客和博客上的动态，整理成每日/每周可消化的摘要。

## 核心功能

- **多源聚合**：X/Twitter 动态、AI 播客（含完整转录）、官方博客（Claude Blog、Anthropic 工程博客等）
- **智能摘要**：AI 摘要 + 多语言翻译（含中文）
- **多渠道分发**：Telegram、Discord、WhatsApp、邮件
- **隐私友好**：中央集中抓取（每日更新），无需用户提供 API 密钥
- **本地配置**：用户偏好存储在 `~/.follow-builders/config.json`

## 监控的构建者

包括 Andrej Karpathy、Swyx、Josh Woodward、Kevin Weil、Sam Altman 等知名 AI 研究员、创始人和工程师。

## 技术架构

- **确定性数据流**：独立爬虫脚本生成单一 JSON 数据块，Claude 仅负责内容处理和分发
- **数据源**：RSS + 网络爬虫（博客）、YouTube 转录 API（播客）、X/Twitter API
- **跨平台**：兼容 Claude Code、OpenClaw、Cursor 等

## 为什么值得关注

在信息噪声爆炸的 AI 领域，精选来自真正建设者的深度见解。同时也是一个复杂 Claude Skill 的典范——涵盖数据管理、用户偏好、跨平台支持。

## 相关链接

- GitHub: https://github.com/zarazhangrui/follow-builders
