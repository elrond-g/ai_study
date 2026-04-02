# Ladybird

> GitHub | https://github.com/LadybirdBrowser/ladybird

## 项目简介

Ladybird 是一款真正独立的 Web 浏览器，使用全新自研引擎，不基于 Chromium/Gecko/WebKit，完全从零构建，目标是实现现代 Web 标准。目前处于 pre-alpha 阶段，62K+ Stars。

## 核心特点

- **完全独立引擎**：不依赖任何现有浏览器内核，从零实现
- **多进程架构**：主 UI 进程 + 多个 WebContent 渲染进程 + ImageDecoder 进程 + RequestServer 进程
- **安全沙盒**：图像解码和网络连接在独立进程中运行，每个标签页拥有独立的沙盒渲染进程
- **跨平台**：支持 Linux、macOS、Windows (WSL2) 及其他 *Nix 系统

## 核心组件（源自 SerenityOS）

| 组件 | 功能 |
|------|------|
| LibWeb | Web 渲染引擎 |
| LibJS | JavaScript 引擎 |
| LibWasm | WebAssembly 实现 |
| LibCrypto/LibTLS | 加密和 TLS |
| LibHTTP | HTTP/1.1 客户端 |
| LibGfx | 2D 图形库和图像解码 |
| LibUnicode | Unicode 和本地化支持 |
| LibMedia | 音视频播放 |
| LibCore | 事件循环和 OS 抽象层 |
| LibIPC | 进程间通信 |

## 技术规格

- **语言**：C++
- **许可证**：BSD 2-Clause
- **Stars**：62,000+

## 相关链接

- GitHub: https://github.com/LadybirdBrowser/ladybird
- 官网: https://ladybird.org
