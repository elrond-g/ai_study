# Qwopus3.5-27B-v3-GGUF

> HuggingFace | https://huggingface.co/Jackrong/Qwopus3.5-27B-v3-GGUF

## 项目简介

Qwopus3.5-27B-v3 是基于 Qwen3.5-27B 的推理增强模型的 GGUF 量化版本，由 Jackrong 开发。v3 版本相比 v2（纯蒸馏）进行了结构性推理对齐优化，同时加入了工具调用的强化学习训练，专为 Agent 框架（如 OpenClaw）优化。

## 核心理念

> **范式转换**：从 "先推理再行动"（reason-then-act）→ "先行动再优化"（act-then-refine）

Agent 性能应通过执行驱动的优化循环提升——轻量初始推理、环境中执行、基于反馈迭代优化。

## v3 vs v2 对比

| | v2（蒸馏） | v3（结构对齐） |
|---|---|---|
| CoT 来源 | 第三方蒸馏轨迹 | 经筛选的可验证推理链 |
| 学习目标 | 模仿教师输出 | 学习过程级推理 |
| 推理风格 | 压缩的、可能虚构的 | 显式的、逐步的、忠实的 |
| 鲁棒性 | 在未见任务上较低 | 更高的泛化能力 |

## 关键特点

- **结构化推理优化**：通过高质量推理蒸馏和结构对齐，以更短更稳定的推理路径实现更高准确率
- **工具调用强化**：专门的 RL 训练优化工具调用稳定性，针对 OpenClaw 等 Agent 框架
- **Act-Then-Refine 范式**：为复杂多步 Agent 工作流设计

## Benchmark 成绩

### HumanEval 164 题完整评测

| 模型 | Base Pass | Plus Pass | vs Qwen3.5-27B |
|------|-----------|-----------|----------------|
| 🥇 Qwopus3.5-27B-v3 | **97.56%** (160/164) | **95.73%** (157/164) | +1.22 pp |
| Qwen3.5-27B | 95.73% (157/164) | 94.51% (155/164) | — |
| Claude-Distilled-v2 | 95.12% (156/164) | 92.68% (152/164) | -1.83 pp |

## 模型规格

- **基础模型**：Qwen3.5-27B
- **格式**：GGUF（量化部署友好）
- **训练方式**：SFT + LoRA + RL（工具调用）
- **支持语言**：中文、英文、韩文
- **许可证**：Apache 2.0
- **Likes**：84

## 相关链接

- GGUF: https://huggingface.co/Jackrong/Qwopus3.5-27B-v3-GGUF
- 基础模型: https://huggingface.co/Qwen/Qwen3.5-27B
- 前版: https://huggingface.co/Jackrong/Qwen3.5-27B-Claude-4.6-Opus-Reasoning-Distilled
