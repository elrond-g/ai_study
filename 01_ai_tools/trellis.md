# Trellis

开箱即用的 AI 编程工程化框架。Trellis 将 Specs（规范）、Tasks（任务）、Memory（记忆）持久化到仓库中，让任何 Coding Agent 都遵循团队工程标准，解决 AI 编码"每次从零开始"的痛点。

## 核心特性

### 自动化规范注入（Auto-injected Specs）

在 `.trellis/spec/` 中编写一次工程规范，Trellis 自动将相关上下文注入每次 AI 编码会话，避免重复说明项目约定。

### 任务中心化工作流

PRD、实现上下文、审查上下文和任务状态统一存放在 `.trellis/tasks/`，确保 AI 编码工作结构化、可追溯。

### 项目记忆（Project Memory）

`.trellis/workspace/` 中的日志记录上次会话发生了什么，让每次新会话都从真实上下文开始，而非空白状态。

### 团队共享标准

Specs 文件随 Git 仓库版本化管理，一个人的最佳实践可惠及整个团队。

### 多平台支持

同一套 Trellis 结构可应用于 14 个 AI 编程平台（Claude Code、Cursor、Codex、OpenCode、Gemini CLI、Hermes 等），无需为每个工具重新配置。

## 工作流（4 阶段循环）

| 阶段 | 说明 |
|------|------|
| **Plan（规划）** | `trellis-brainstorm` 逐步梳理需求，生成 `prd.md`；复杂项交给 `trellis-research` 子 Agent 调研 |
| **Implement（实现）** | `trellis-implement` 子 Agent 依据 PRD 和自动注入的上下文写代码，不自动 git commit |
| **Verify（验证）** | `trellis-check` 子 Agent 对照 Specs 审查 diff，运行 lint/type-check/tests，自动修复问题 |
| **Finish（收尾）** | 最终检查后，`trellis-update-spec` 将新学到的经验提升到 `.trellis/spec/`，下次会话更智能 |

## 技术架构

- **语言**：TypeScript/Node.js（CLI 主体）+ Python 辅助
- **安装方式**：npm 全局包 `@mindfoldhq/trellis`
- **运行环境**：Node.js >= 18，Python >= 3.9
- **许可证**：AGPL-3.0
- **存储结构**：基于文件系统的 `.trellis/` 目录，与 Git 天然集成

## 安装与使用

```bash
# 安装
npm install -g @mindfoldhq/trellis@latest

# 在项目中初始化
trellis init -u your-name

# 指定平台初始化
trellis init --cursor --opencode --codex -u your-name

# 工作流程
# 1. 用自然语言描述需求
# 2. 与 AI 逐步 Brainstorm 直至 PRD 清晰
# 3. AI 自动调用 Implement → Verify 循环
# 4. 输入 /trellis:finish-work 收尾归档
```

## 与 CLAUDE.md / .cursorrules 的区别

传统配置文件（CLAUDE.md、AGENTS.md、.cursorrules）容易变得臃肿单一。Trellis 在其基础上增加了：作用域化 Specs、任务 PRD、工作流闸门（gate）、工作区记忆、平台感知的生成文件。

## GitHub

https://github.com/mindfold-ai/Trellis
