# My-Brain-Is-Full-Crew

> ⭐ 2.5k+ | Shell | https://github.com/gnekt/My-Brain-Is-Full-Crew | MIT

## 项目简介

My-Brain-Is-Full-Crew 是一个基于 8+ AI Agent 和 14 个专业技能的 Obsidian 知识管理系统。由一位记忆力衰退的博士研究员创建，核心理念：不只是知识扩展，而是"大脑倾倒系统"——管理知识、身体健康和心理状态。用户只需用自然语言对话，Agent 自动完成笔记整理、分类、搜索、转录和邮件分诊。

## Agent 团队

| # | Agent | 角色 | 能力 |
|---|-------|------|------|
| 1 | Architect | 仓库结构与设置 | 设计整个 Vault、运行引导、制定规则 |
| 2 | Scribe | 文本捕获 | 将混乱的意识流转为干净笔记 |
| 3 | Sorter | 收件箱分诊 | 每晚清空收件箱，路由笔记到合适位置 |
| 4 | Seeker | 搜索与智能 | 跨笔记检索、综合回答并附引用 |
| 5 | Connector | 知识图谱 | 发现笔记间隐藏的关联 |
| 6 | Librarian | 仓库维护 | 周度健康检查、去重、修复断链 |
| 7 | Transcriber | 音频与会议 | 将录音/转录转为结构化会议笔记 |
| 8 | Postman | 邮件与日历 | 桥接 Gmail/Hey.com 和 Google Calendar |

## 14 个 Skills

包括 `/onboarding`（完整 Vault 设置）、`/create-agent`（自定义 Agent 创建向导）、`/email-triage`（邮件分诊）、`/meeting-prep`（会议准备）、`/transcribe`（录音处理）、`/vault-audit`（7 阶段审计）、`/deep-clean`（深度清理）、`/tag-garden`（标签整理）等。

## 工作原理

```
用户对话 → Dispatcher 检查 Skills → 匹配则调用 Skill
                                  → 不匹配则调用 Agent → Vault 自动更新
```

Dispatcher 双层委派：Skills 处理复杂多步对话流程（引导、邮件分诊、审计），Agents 处理快速单次操作（捕获笔记、搜索、创建文件夹）。每个 Agent 是独立 AI，拥有自己的系统提示、工具限制和模型分配。

## 核心特点

- **对话即界面**：不需要手动浏览 Obsidian、拖拽文件或维护文件夹结构
- **多语言原生支持**：任何语言对话，Agent 自动匹配
- **Agent 链式协作**：转录 Agent 处理会议发现新项目时，Dispatcher 自动链接 Architect 创建文件夹结构
- **自定义 Agent**：通过对话设计新 Agent，无需代码，自动融入团队协作

## 为什么值得关注

区别于大多数"AI + 笔记"工具只做知识优化，这个项目面向信息过载、精力枯竭的人群。8 Agent + 14 Skills 的完整团队编排、Dispatcher 双层委派、自定义 Agent 创建向导，展示了成熟的多 Agent 知识管理架构。

## 相关链接

- GitHub: https://github.com/gnekt/My-Brain-Is-Full-Crew
