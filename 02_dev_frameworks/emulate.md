# Emulate

> ⭐ 929 | TypeScript | https://github.com/vercel-labs/emulate

## 项目简介

Emulate 是 Vercel Labs 出品的本地 API 仿真服务，为 CI 和无网络沙箱环境提供 Vercel/GitHub/AWS/Slack 等主流平台的全状态 API 替身。`npx emulate` 一键启动，为 AI Agent 在沙箱中执行任务提供离线 API 环境。

## 核心功能

- **主流平台仿真**：覆盖 Vercel、GitHub、AWS、Slack 等平台 API
- **全状态模拟**：不只是 Mock，提供有状态的完整 API 行为
- **一键启动**：`npx emulate` 零配置快速运行
- **CI 友好**：可直接集成到持续集成流水线
- **沙箱支持**：为无网络环境（如 Codex 沙箱）提供 API 访问

## 技术特点

- TypeScript 实现
- 本地运行，无需外部依赖
- 支持多平台 API 的同时模拟

## 使用场景

- AI Agent（如 Codex）在沙箱环境中执行涉及外部 API 的任务
- CI/CD 管道中的集成测试替代真实 API
- 本地开发时模拟第三方服务

## 相关链接

- GitHub: https://github.com/vercel-labs/emulate
