# AI Agent Deep Dive（AI Agent 源码深度研究）

> GitHub | https://github.com/tvytlx/claude-code-deep-dive

## 项目简介

AI Agent 源码深度研究报告，通过逆向分析 Claude Code 等 AI Agent 的内部实现，输出详尽的技术分析 PDF。同时包含一个教学用的最小 Python Agent 项目，演示 AI Agent 的核心结构。3,900+ Stars。

## 核心内容

### 深度分析报告

- 最新版 `ai-agent-deep-dive-v2.pdf`
- 仅保留面向学习与评论的分析材料，不提供源码目录

### 教学用最小 Agent 项目

一个为教学设计的最小 Python Agent 实现：

- **Agent 核心代码**：`src/agt/agent.py` — Agent 主循环
- **CLI 入口**：`src/agt/cli.py` — 命令行接口
- **教学文档**：`docs/` — 详细说明

### 设计特点

- 结构清晰，减少不必要的工程复杂度
- 核心代码集中在很小的范围内，方便学习
- 重点覆盖：Agent 主循环、Fake LLM 接口、Skills 发现、CLI 骨架
- 内置可替换的 Fake LLM，后续接入真实模型只需替换 LLM 调用层

## 快速运行

```bash
poetry install
poetry run agt "你好"
poetry run agt --skills-dir ./skills --list-skills
```

## 技术规格

- **语言**：Python
- **依赖管理**：Poetry
- **Stars**：3,900+

## 相关链接

- GitHub: https://github.com/tvytlx/claude-code-deep-dive
