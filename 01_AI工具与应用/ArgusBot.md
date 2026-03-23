# ArgusBot

> ⭐ 256 | Python | https://github.com/waltstephen/ArgusBot

## 项目简介

ArgusBot 是一个 24/7 持续监控的 AI Agent 监督者，专门用于管理 Codex CLI 和 Claude Code CLI 等 AI 编程工具的执行过程。它像一个永不下线的 QA 工程师，持续审查 Agent 的工作、规划下一步、确保任务真正完成而不是被草草了事。

## 核心功能

- **全程监督**：监控 AI Agent 的每一步操作，防止任务中途停滞或偏轨
- **持续规划**：在 Agent 完成当前步骤后，自动评估进度并规划下一步
- **质量审查**：对 Agent 生成的代码和决策进行实时 review
- **自动重启**：检测到 Agent 卡死或出错时自动恢复执行

## 技术特点

- Python 实现，轻量部署
- 与 Codex CLI、Claude Code CLI 深度集成
- 基于循环监控架构，持续轮询 Agent 状态

## 使用场景

- 长时间运行的自动化编程任务，需要稳定的监督机制
- 防止 AI Agent 在复杂任务中"自以为完成"却实际未完成
- 团队希望在无人值守时让 AI Agent 持续工作

## 相关链接

- GitHub: https://github.com/waltstephen/ArgusBot
