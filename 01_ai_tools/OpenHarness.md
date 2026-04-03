# OpenHarness

> GitHub | https://github.com/HKUDS/OpenHarness

## 项目简介

OpenHarness 是一个开源的轻量级 Agent 基础设施框架，提供工具调用、Skills、记忆和多 Agent 协调等核心能力。一条命令 `oh` 即可启动，支持 OpenClaw、nanobot、Cursor 等 CLI Agent 集成。1,200+ Stars，港大 HKUDS 出品。

## 核心特性

### Agent Loop（Agent 循环）
- 流式工具调用循环
- API 指数退避重试
- 并行工具执行
- Token 计数与费用追踪

### Harness Toolkit（工具集）
- 43+ 工具（文件/Shell/搜索/Web/MCP）
- 按需加载 Skill（.md 格式）
- 插件生态（Skills + Hooks + Agents）
- 兼容 anthropics/skills 和 plugins

### Context & Memory（上下文与记忆）
- CLAUDE.md 发现与注入
- 上下文压缩（Auto-Compact）
- MEMORY.md 持久化记忆
- 会话恢复与历史

### Governance（治理）
- 多级权限模式
- 路径级与命令级规则
- PreToolUse / PostToolUse Hooks
- 交互式审批对话框

### Swarm Coordination（多 Agent 协调）
- 子 Agent 生成与委派
- 团队注册与任务管理
- 后台任务生命周期
- ClawTeam 集成（路线图）

## 技术规格

- **语言**：Python ≥3.10（后端）+ React+Ink（TUI）
- **测试**：114 通过 + 6 个 E2E 测试套件
- **输出格式**：text / json / stream-json
- **许可证**：MIT
- **Stars**：1,200+

## 相关链接

- GitHub: https://github.com/HKUDS/OpenHarness
- ClawTeam: https://github.com/HKUDS/ClawTeam
