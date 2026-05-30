# oh-my-pi (omp)

终端 AI Coding Agent，将 IDE 能力内置于命令行。在 Pi 项目基础上大幅增强，支持 40+ 模型提供商、32 个内置工具、13 种 LSP 操作、27 种 DAP 操作，约 27k 行 Rust 核心代码。

## 核心特性

### 极致工具优化
每种工具都经过精心调优——编辑一次命中、文件阅读自动总结而非全文转储、搜索即时返回。对 Grok Code Fast 1 等模型的性能提升高达 10 倍。

### IDE 级能力
内置 LSP 支持（13 种操作）和调试协议 DAP（27 种操作），终端内即可实现跳转定义、查找引用、设置断点等 IDE 操作。

### Hash-Anchored 编辑
独特的 hash 锚点编辑方案，在多文件修改场景下保持编辑精确定位。

### 广泛的模型支持
40+ 模型提供商，包括 OpenAI、Anthropic、Google、xAI、DeepSeek 等。

## 技术架构

- **核心语言**：Rust（~27k 行）+ TypeScript
- **运行时**：Bun
- **工具**：32 个内置工具 + 浏览器 + Python + 子 Agent
- **平台**：macOS / Linux / Windows

## 安装与使用

```bash
# 安装
curl -fsSL https://omp.sh/install | sh

# 或使用 Bun
bun install -g @oh-my-pi/pi-coding-agent
```

## GitHub

https://github.com/can1357/oh-my-pi
