# ghost-os

> ⭐ 1,205 | Swift | https://github.com/ghostwright/ghost-os

## 项目简介

ghost-os 为 AI Agent 提供完整的 macOS 计算机操作能力（Computer Use），无需截图即可控制任何应用程序。基于 macOS Accessibility API，实现对 UI 元素的精准感知和操控，并支持自学习工作流程。

## 核心功能

- **全 macOS Computer Use**：控制任意 macOS 应用，不依赖视觉截图
- **Accessibility API 驱动**：通过系统辅助功能 API 精准识别和操作 UI 元素
- **自学习工作流**：Agent 可记录和复用操作序列，形成可重复执行的 Recipe
- **MCP 集成**：作为 MCP Server 被 Claude Code 等工具调用
- **无截图架构**：相比 computer use 截图方案，响应更快、精度更高

## 技术特点

- Swift 原生开发，深度集成 macOS 系统能力
- 基于 Accessibility API，而非图像识别——速度和准确度更高
- Claude Code 深度集成，可直接在 AI 编程流程中控制桌面应用

## 使用场景

- AI Agent 控制 Xcode、Figma 等无 API 的桌面应用
- 自动化 macOS 工作流（邮件处理、文件整理等）
- 为 LLM 提供真实的计算机操作能力

## 相关链接

- GitHub: https://github.com/ghostwright/ghost-os
