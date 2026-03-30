# yoyo-evolve

> ⭐ 563+ | Rust | https://github.com/yologdev/yoyo-evolve

## 项目简介

yoyo-evolve 是一个自进化代码代理（Self-Evolving Coding Agent）。创作者用 200 行 Rust CLI 启动实验，给予 Agent 一个不变的目标：进化成能与 Claude Code 竞争的开源代码代理。采用"楚门的世界"式设计——自动化循环让 Agent 自己读取源码、检查 Issue、规划改进、实现变更、测试并提交。

## 自进化成果

24 天自主进化后：
- 31,000+ 行 Rust 代码
- 1,346 个测试用例
- 14 个代码模块
- 完全由 Agent 自主完成，无人类编写代码

## 核心功能

- **55 个斜杠命令**：代码导航、多文件编辑、测试运行、Git 操作
- **自主进化循环**：每 ~8 小时自动唤醒，读取自身源码 → 检查 GitHub Issues → 规划改进 → 实现 → 测试 → 提交/回滚
- **社交学习**：每 4 小时读取 GitHub Discussions，参与对话并从社区学习
- **时间加权记忆**：每日重新生成活动内存，近期记忆保留完整，旧记忆归纳为主题
- **项目上下文**：自动加载 YOYO.md（或 CLAUDE.md）作为系统提示

## 技术架构

14 个模块：main.rs（入口）、cli.rs（CLI 解析）、commands.rs（命令分发）、git.rs（Git 操作）、memory.rs（记忆系统）、prompt.rs（提示构建）、repl.rs（REPL 循环 + Tab 补全）等。自进化循环由 GitHub Actions 驱动。

## 为什么值得关注

这是一个活生生的 AI 自我进化实验——完整进化历史记录在 Git 日志中，社区可通过 Issues 和 Discussions 影响 Agent 的发展方向。展示了 AI Agent 自主学习、自反省和自改进的能力边界。

## 相关链接

- GitHub: https://github.com/yologdev/yoyo-evolve
- 项目日志: https://yologdev.github.io/yoyo-evolve/
- HN 讨论: https://news.ycombinator.com/item?id=47254139
