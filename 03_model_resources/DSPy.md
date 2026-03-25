# DSPy

> ⭐ 22k+ | Python | https://github.com/stanfordnlp/dspy

## 项目简介

斯坦福大学出品的 LLM 编程框架，用声明式方式编写 prompt pipeline 并自动优化。告别手写 prompt，让框架自动搜索最优提示策略。

## 核心功能

- **声明式签名（Signatures）**：用简洁的类型签名定义输入输出，框架自动生成最优 prompt
- **自动优化器（Optimizers）**：基于少量标注数据自动调优 prompt 和示例选择策略
- **模块化流水线（Modules）**：像搭积木一样组合 ChainOfThought、ReAct 等推理模块

## 技术特点

- 将 prompt engineering 转化为可编程、可优化的工程问题
- 支持 OpenAI、Anthropic、本地模型等多种后端
- 内置评估与断言机制，保障输出质量

## 使用场景

- 构建多步骤 RAG 检索问答系统
- 自动优化复杂 Agent 工作流中的提示策略
- 快速迭代 NLP 任务而无需反复手调 prompt

## 相关链接

- GitHub: https://github.com/stanfordnlp/dspy
