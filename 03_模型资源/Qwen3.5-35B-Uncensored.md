# Qwen3.5-35B-Uncensored

> HuggingFace | https://huggingface.co/HauhauCS/Qwen3.5-35B-A3B-Uncensored-HauhauCS-Aggressive

## 项目简介

Qwen3.5-35B-Uncensored 是基于通义千问 3.5（35B 参数，MoE 架构激活参数约 3B）的去除安全审查版本，由 HauhauCS 使用 Abliteration 技术处理，采用"Aggressive"强度设置，彻底移除模型的各类拒绝和限制行为。

## 模型规格

- **基础模型**：Qwen3.5-35B-A3B（35B 总参数，MoE 架构）
- **激活参数**：约 3B（推理成本接近 3B 模型）
- **处理方式**：Aggressive Abliteration（最高强度去审查）
- **格式**：HuggingFace 标准格式，可直接加载

## 技术特点

- 使用 MoE（混合专家）架构：总参数量大但推理成本低
- Aggressive 模式意味着更彻底的审查移除，但可能轻微影响一般能力
- 基础模型 Qwen3.5 本身具有强大的中英文能力

## 硬件需求

| 量化精度 | 显存需求 |
|---------|---------|
| FP16 | ~70GB |
| Q8 | ~35GB |
| Q4 | ~18GB |

## 使用场景

- 研究 LLM 安全对齐与能力之间的权衡
- 需要无限制输出的学术和安全研究
- 对比审查前后模型行为的差异

## 相关链接

- HuggingFace: https://huggingface.co/HauhauCS/Qwen3.5-35B-A3B-Uncensored-HauhauCS-Aggressive
