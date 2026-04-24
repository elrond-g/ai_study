# Obscura

> ⭐ 1.7K+ | Rust | https://github.com/h4ckf0r0day/obscura

## 项目简介

Obscura 是 Rust 编写的开源无头浏览器引擎，专为 AI Agent 和网页爬虫设计。通过 V8 运行真实 JavaScript，支持 Chrome DevTools Protocol，可作为 Puppeteer / Playwright 的 Drop-in 替代，内存占用仅 30MB（对比 Chrome 200MB+）。

## 核心功能

- **极致轻量**：内存 30MB、二进制 70MB、页面加载 85ms，启动瞬时（对比 Chrome 约 2 秒）
- **Puppeteer / Playwright 兼容**：实现 CDP 协议（Target/Page/Runtime 等），现有自动化脚本无需改动
- **内置 Stealth 模式**：反检测指纹随机化（GPU/屏幕/canvas/audio/battery）+ 3520 域名追踪阻断，`navigator.webdriver = undefined`

## 技术特点

- Rust + V8，单二进制无依赖（不需要 Chrome、Node.js）
- 支持并发批量抓取（`--concurrency 25`）、表单提交、Cookie 维护、302 跳转
- 原生函数伪装（`Function.prototype.toString()` 返回 `[native code]`），`event.isTrusted = true`

## 使用场景

- AI Agent 大规模网页操控（低内存 + 反封禁）
- 网页爬虫对抗反爬检测（替代 puppeteer-stealth）
- CI / 资源受限环境下的网页自动化测试

## 相关链接

- GitHub: https://github.com/h4ckf0r0day/obscura
