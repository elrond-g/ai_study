# last30days-skill

> ⭐ 1.5k+ | Node.js + SQLite | https://github.com/mvanhorn/last30days-skill | MIT

## 项目简介

last30days-skill 是一个实时研究引擎 Skill，自动扫描过去 30 天内 10+ 个社区平台的讨论内容，生成经过验证和引用的综合报告。核心理念："30 天的研究成果，30 秒的工作量"。

## 支持的数据源

Reddit、X/Twitter、Bluesky、YouTube、TikTok、Instagram、Hacker News、Polymarket、网络搜索等 10+ 平台

## 核心功能

- **多平台并行搜索**：同时搜索多个社区平台的近 30 天内容
- **社区情感分析**：识别社区真正在点赞、分享、讨论的内容
- **智能排序去重**：多信号相关性评分 + 跨平台收敛算法
- **对比模式**：支持 "X vs Y" 类型的对比研究
- **持久化存储**：SQLite 数据库累积发现，支持定时任务重复研究
- **自动保存**：研究简报自动保存至 `~/Documents/Last30Days/`

## 输出内容

最佳实践、可复用提示词、工作流建议和专家级答案，全部附带来源引用。

## 技术栈

- Node.js 22+
- SQLite（历史数据和缓存）
- OpenAI Responses API（Reddit 搜索）、xAI Responses API（X 搜索）
- 支持 Claude Code、Codex CLI、Gemini CLI

## 使用方式

在 Claude Code 中使用 `$last30days` 命令调用，或通过 `/skills` 菜单。支持与 cron 任务集成实现自动化研究。

## 为什么值得关注

解决了 AI 技术快速演进的痛点——提供基于当前社区共识而非过时训练数据的答案。覆盖 10+ 平台的实时研究能力在 Skill 生态中独树一帜。

## 相关链接

- GitHub: https://github.com/mvanhorn/last30days-skill
