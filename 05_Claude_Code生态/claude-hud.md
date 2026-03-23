# claude-hud

> https://github.com/jarrodwatts/claude-hud

## 项目简介

claude-hud 是一个 Claude Code 运行状态可视化工具，在终端或独立窗口中提供实时的 HUD（抬头显示）界面，清晰展示 Claude Code 当前的工作状态、token 使用量、成本统计和任务进度。

## 核心功能

- **实时状态显示**：当前 Claude Code 正在执行的操作
- **Token 用量监控**：输入/输出 token 的实时计数
- **成本追踪**：按会话统计 API 调用费用
- **任务进度**：多步骤任务的完成进度可视化
- **工具调用日志**：记录 Claude Code 调用的每个工具

## 技术特点

- 轻量级后台进程，不影响 Claude Code 性能
- 终端 UI 设计，无需额外窗口
- 数据实时更新，低延迟

## 使用场景

- 长时间运行的 Claude Code 任务中监控进度
- 控制 API 使用成本，避免意外超支
- 调试 Claude Code 工作流，了解每个步骤的资源消耗

## 相关链接

- GitHub: https://github.com/jarrodwatts/claude-hud
