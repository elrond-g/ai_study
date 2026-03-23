# page-agent

> ⭐ 13,500+ | TypeScript | https://github.com/alibaba/page-agent | https://alibaba.github.io/page-agent/

## 项目简介

page-agent 是阿里巴巴开源的 JavaScript 网页内 GUI Agent，让 AI 可以通过自然语言直接操控网页界面。与传统浏览器自动化（Selenium/Playwright）不同，page-agent 在页面内部运行，通过理解 DOM 结构和视觉元素来精准执行用户指令。

## 核心功能

- **自然语言控制**：用中文或英文描述操作，Agent 自动找到对应元素并执行
- **In-page 执行**：直接嵌入网页运行，无需外部浏览器驱动
- **MCP 协议支持**：可作为 MCP Server 被 AI 工具调用
- **跨框架兼容**：支持 React、Vue、原生 HTML 等各类网页

## 技术特点

- TypeScript 实现，支持 ESM/CommonJS
- 结合视觉感知与 DOM 分析双重理解机制
- 内置动作执行引擎（点击、输入、滚动、截图等）

## 使用场景

- 构建能够操控 Web 应用的 AI Agent
- 自动化表单填写、数据抓取、界面测试
- 为 AI 助手提供"操作浏览器"的能力

## 相关链接

- GitHub: https://github.com/alibaba/page-agent
- 文档: https://alibaba.github.io/page-agent/
