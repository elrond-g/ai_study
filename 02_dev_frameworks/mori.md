# mori

> ⭐ 100 | Swift | https://github.com/vaayne/mori

## 项目简介

mori 是一个原生 macOS 工作区终端，专门围绕 Git 项目和 Worktree 来组织终端会话。由 tmux 和 libghostty 驱动，为 AI 辅助开发（尤其是多 worktree 并行工作模式）提供专属的终端体验。

## 核心功能

- **Worktree 中心化管理**：将 Git Worktree 作为工作区的核心组织单元
- **项目感知**：终端会话与 Git 项目绑定，切换项目即切换完整工作环境
- **tmux 集成**：基于 tmux 的会话管理，支持窗口和面板分割
- **libghostty 驱动**：使用 Ghostty 终端引擎，高性能渲染

## 技术特点

- Swift 原生开发，macOS 深度集成
- Worktree + tmux 双层架构，隔离不同任务的工作环境
- 专为 AI 辅助多任务并行场景优化

## 为什么值得关注

Claude Code 等 AI 工具推荐用 Git Worktree 隔离并行任务，但传统终端对 worktree 的管理体验很差。mori 填补了这个空白，让多 worktree 工作流变得顺畅自然。

## 相关链接

- GitHub: https://github.com/vaayne/mori
