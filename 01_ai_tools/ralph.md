# Ralph

> ⭐ 17.5k | MIT | https://github.com/snarktank/ralph

## 项目简介

自主 AI Agent 循环器，接收一份 PRD（Product Requirements Document），然后不断派生干净上下文的新实例（Amp 或 Claude Code）迭代执行，直到任务完成。记忆通过 Git 历史 + 进度文件 + 任务状态持久化，而非上下文窗口。

## 核心特性

- **自主迭代**：每轮启动全新 Agent 实例，避免上下文漂移
- **PRD 生成与 JSON 转换**：自然语言需求自动结构化
- **质量门**：每次提交前自动 typecheck + tests
- **进度跟踪**：进度文件 + 学习日志持久化
- **多 Agent 后端**：同时支持 Amp 和 Claude Code
- **交互流程图**：可视化迭代状态

## 核心理念

"Right-sized stories"——每个故事控制在单个上下文窗口内，反馈循环确保可靠的自主执行。借鉴软件工程中的小步快跑 + CI/CD 思想。

## 技术栈

- TypeScript 62.9% + Shell 17.6%
- 支持 Amp（Sourcegraph）和 Claude Code 双后端
- Git 为核心记忆介质

## 与其他 Autoresearch 对比

- 与 Karpathy autoresearch 思路一致：自主循环 + 新鲜上下文
- 区别：Ralph 显式以 PRD 为输入、以 Git 为记忆，工程化程度更高
- 同类：pi-autoresearch（Shopify CEO）、yoyo-evolve

## 相关链接

- GitHub: https://github.com/snarktank/ralph
