# oh-my-openagent

> ⭐ 42,987 | TypeScript | https://github.com/code-yeongyu/oh-my-openagent

## 项目简介

定位为"最佳 Agent 执行框架"（omo），前身为 oh-my-opencode。提供统一的 Agent Harness，可将 Claude Code、Codex、OpenCode 等各类 AI 编程代理接入同一套执行环境，并提供中文使用文档。

## 核心功能

- **统一 Agent 接口**：对接 Claude Code、Codex、Cursor 等多种 AI 编程工具
- **Harness 层**：在 Agent 执行上层提供拦截、监控、重试等统一能力
- **中文文档**：提供完整中文 README，降低国内开发者使用门槛
- **TypeScript 实现**：类型安全，便于二次开发扩展

## 技术特点

- 基于 TypeScript，Node.js 生态，无需额外运行时
- Harness 设计模式：把 Agent 调用包裹在可扩展的执行层中
- 与 ACP（Agent Client Protocol）协议兼容

## 使用场景

- 需要在多个 AI 编程工具之间切换或对比的开发者
- 想在 Agent 执行过程中注入自定义逻辑（日志、限流、拦截）
- 构建企业级 AI 编程基础设施

## 相关链接

- GitHub: https://github.com/code-yeongyu/oh-my-openagent
