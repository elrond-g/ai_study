# autoresearch

> ⭐ 51,000+ | Python | https://github.com/karpathy/autoresearch

## 项目简介

autoresearch 是 Andrej Karpathy 开源的 AI 自动研究框架，核心能力是让 AI Agent 在单张 GPU 上自动运行 NanoChat 模型训练实验并提炼研究结论。这是一个将 AI 用于 AI 研究本身的元级项目——Agent 自主设计实验、运行训练、分析结果、迭代假设。

## 核心功能

- **全自动实验循环**：从研究问题出发，自动设计、运行、评估实验
- **单 GPU 适配**：专为消费级 GPU 优化，无需多机集群
- **NanoChat 训练**：内置轻量语言模型训练流水线
- **结果分析与迭代**：Agent 基于实验结果自动调整下一步方向

## 技术特点

- Karpathy 一贯的极简代码风格，核心逻辑清晰可读
- Python + PyTorch 技术栈
- 实验结果自动记录，支持可复现性

## 使用场景

- AI 研究人员希望用 Agent 加速模型迭代实验
- 学习如何将 Agent 框架应用于科学研究场景
- 探索"AI 自我研究"（self-improvement research）方向

## 相关链接

- GitHub: https://github.com/karpathy/autoresearch
