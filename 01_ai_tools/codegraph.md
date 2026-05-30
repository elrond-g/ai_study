# CodeGraph

代码知识图谱预索引工具，为 Claude Code、Cursor、Codex、OpenCode、Hermes Agent 等 AI 编程智能体提供语义代码智能。声称节省约 25% Token 消耗、减少约 62% 工具调用，100% 本地运行。

## 核心特性

### 预索引知识图谱
在 Agent 启动前预先构建代码关系图，避免 Agent 反复搜索和阅读文件，大幅降低 Token 消耗。

### 多 Agent 支持
原生支持 Claude Code、Cursor、Codex CLI、OpenCode、Hermes Agent、Gemini CLI、Antigravity、Kiro 八种主流 AI 编程工具。

### 零依赖安装
内置 Node.js 运行时，一键安装无需额外配置。跨平台支持 Windows、macOS、Linux。

### 语义索引
不只是文本匹配，支持符号级别的代码索引，Agent 可以直接查询函数签名、类型定义、调用关系。

## 技术架构

- **运行时**：内置 Bun/Node.js，无需系统安装 Node
- **安装方式**：curl 一键安装脚本 或 npx/npm
- **存储**：本地 `.codegraph/` 目录，完全离线

## 安装与使用

```bash
# 安装
curl -fsSL https://raw.githubusercontent.com/colbymchenry/codegraph/main/install.sh | sh

# 初始化项目
cd your-project
codegraph init -i
```

## GitHub

https://github.com/colbymchenry/codegraph
