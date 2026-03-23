# Lightpanda Browser

> ⭐ 24,000+ | Zig | https://github.com/lightpanda-io/browser | https://lightpanda.io

## 项目简介

Lightpanda 是专门为 AI 和自动化场景设计的无头浏览器，用 Zig 语言构建。相比 Chromium 系无头浏览器，Lightpanda 内存占用极小、启动极快，专注于 AI Agent 最需要的功能：DOM 操作、JavaScript 执行和页面内容提取。

## 核心功能

- **极致轻量**：内存占用仅为 Chromium 无头模式的 1/10 以下
- **快速启动**：毫秒级冷启动，适合高频并发的 Agent 场景
- **Playwright/Puppeteer 兼容**：支持 CDP 协议，可直接替换现有自动化脚本
- **AI 优化**：内置页面内容结构化提取，减少 AI 处理成本

## 技术特点

- Zig 语言编写，极低内存占用和出色的性能
- 支持 Chrome DevTools Protocol (CDP)
- 原生支持 JavaScript 执行环境

## 使用场景

- 大规模并发网页抓取和内容提取
- AI Agent 的浏览器工具层（低成本替代 Chrome）
- 网页自动化测试（对资源消耗敏感的 CI 环境）

## 相关链接

- GitHub: https://github.com/lightpanda-io/browser
- 官网: https://lightpanda.io
