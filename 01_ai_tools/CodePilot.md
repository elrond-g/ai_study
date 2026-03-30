# CodePilot

> ⭐ 4,447+ | Electron + Next.js | https://github.com/op7418/CodePilot | https://www.codepilot.sh/

## 项目简介

CodePilot 是 Claude Code 的原生桌面工作区，基于 Electron + Next.js 构建。从最初的简单 GUI 封装进化为功能完备的桌面 IDE，提供会话检查点、分屏工作、跨平台 Bridge、MCP + Skills 扩展等深度集成功能。最新版本 0.42.0（2026年3月28日）。

## 核心功能

### 会话管理与检查点
- 暂停、恢复和回滚会话到任意检查点
- 每个用户提示自动创建检查点
- 灵活撤销：保留代码回滚对话 / 保留对话撤销代码 / 完全撤销

### 分屏工作模式
- 并行运行两个独立会话，多任务处理

### 工作区配置
- `soul.md`（个性化配置）、`user.md`（用户信息）
- `claude.md`（项目规则）、`memory.md`（持久化记忆）
- Claude 根据这些文件学习项目约定和开发者习惯

### Auto Memory（自动记忆）
- 会话间自动积累知识：构建命令、调试洞察、架构笔记、代码风格偏好
- 状态追踪存储在 `.assistant/` 子目录

### MCP + Skills
- 添加 MCP 服务器（stdio/SSE/HTTP）+ 运行时状态监控
- 自定义 Prompt 式技能（全局/项目级），斜杠命令调用
- 支持从 skills.sh 社区浏览安装

### Bridge 跨平台连接
- Telegram、飞书/Lark、Discord、QQ
- 手机发送消息，桌面获得回复

## 技术栈

| 组件 | 技术 |
|------|------|
| 前端 | Next.js |
| 桌面 | Electron |
| 依赖 | Node.js 18+, npm 9+, Claude Code CLI |
| 平台 | macOS (arm64/amd64), Linux, Windows |

## 为什么值得关注

1. **深度集成**：不是简单的 GUI 壳，而是在 Claude Code 之上构建了完整的工作区体验
2. **检查点系统**：解决了 AI 辅助编程中"改错了想回退"的核心痛点
3. **Bridge 多渠道**：手机端也能操控桌面 Claude Code
4. **活跃迭代**：截至 2026 年 3 月仍在高频发布更新

## 相关链接

- GitHub: https://github.com/op7418/CodePilot
- 官网: https://www.codepilot.sh/
