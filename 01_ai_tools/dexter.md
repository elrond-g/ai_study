# Dexter

> virattt | TypeScript (Bun) | https://github.com/virattt/dexter

## 项目简介

Dexter 是一个轻量级自主金融研究 Agent，仅 ~200 行代码实现完整的多 Agent 金融分析能力。能自主思考、规划和学习，使用实时市场数据执行复杂财务分析。

## 四 Agent 架构

| Agent | 职责 |
|-------|------|
| Planning Agent | 分解高级金融查询为可执行的粒度任务 |
| Action Agent | 通过 Financial Datasets API 获取实时数据 |
| Validation Agent | 严格检查输出的准确性和逻辑连贯性 |
| Answer Agent | 综合验证后的发现生成最终研究输出 |

## 核心特色

- **自我验证**：Agent 审查并迭代改进自己的工作直到结果可信
- **安全机制**：循环检测和步骤限制防止 Agent 失控
- **实时数据**：直接连接 Financial Datasets API（SEC 10-K/10-Q 数据）
- **多 LLM 支持**：OpenAI、Anthropic、Google + 本地 Ollama
- **终端 UI**：React + Ink 实时展示推理过程

## 技术栈

- Bun 运行时 + TypeScript
- Ink（React for CLI）终端 UI
- LangChain.js（Agent 编排）
- LangSmith（追踪和评估）

## 为什么值得关注

~200 行代码实现功能完整的自主金融 Agent，展示了现代 LLM 框架的高效性。自验证机制使其输出比一般 Agent 更可靠，是金融 AI Agent 设计的优秀参考。

## 相关链接

- GitHub: https://github.com/virattt/dexter
