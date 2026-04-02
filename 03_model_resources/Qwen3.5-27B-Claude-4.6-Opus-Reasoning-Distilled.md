# Qwen3.5-27B-Claude-4.6-Opus-Reasoning-Distilled

> HuggingFace | https://huggingface.co/Jackrong/Qwen3.5-27B-Claude-4.6-Opus-Reasoning-Distilled

## 项目简介

Qwen3.5-27B-Claude-4.6-Opus-Reasoning-Distilled 是基于 Qwen3.5-27B 通过 SFT + LoRA 微调的推理增强模型，核心思路是将 Claude 4.6 Opus 的链式思维（CoT）推理能力蒸馏到 Qwen3.5 中，使其在结构化推理、编码和复杂逻辑任务上表现接近 Opus 水平。

## 模型规格

- **基础模型**：Qwen/Qwen3.5-27B（Dense 架构）
- **微调框架**：Unsloth 2026.3.3
- **训练方式**：SFT + LoRA，使用 `train_on_responses_only` 策略
- **推理格式**：`<think> {内部推理} </think>\n {最终回答}`
- **支持语言**：中文、英文
- **上下文窗口**：262K
- **许可证**：Apache 2.0

## 训练数据

| 数据集 | 用途 |
|--------|------|
| nohurry/Opus-4.6-Reasoning-3000x-filtered | Claude 4.6 Opus 推理轨迹蒸馏 |
| TeichAI/claude-4.5-opus-high-reasoning-250x | 高强度结构化推理样本 |
| Jackrong/Qwen3.5-reasoning-700x | 增强推理多样性的补充数据 |

## 技术特点

- 蒸馏 Claude 4.6 Opus 的结构化推理风格："Let me analyze this request carefully: 1..2..3..."
- 优化了 Qwen3.5 在简单查询上过度重复推理的倾向，推理效率显著提升
- 原生支持 "developer" 角色，修复了官方模型因 Jinja 模板不支持该角色导致的崩溃
- 默认不禁用思考模式，Agent 可连续自主运行超过 9 分钟
- 自主性和稳定性大幅提升：主动等待工具响应、读取输出、自我纠错

## 硬件需求（社区实测）

| 量化精度 | 显存需求 | 生成速度 |
|---------|---------|---------|
| Q4_K_M | ~16.5GB | 29-35 tok/s |

## 使用场景

- 本地编码 Agent 环境（Claude Code、OpenCode 等），即插即用
- 离线分析任务、编码、数学和重逻辑推理场景
- 需要透明跟踪 AI 内部推理过程的应用

## 相关链接

- HuggingFace: https://huggingface.co/Jackrong/Qwen3.5-27B-Claude-4.6-Opus-Reasoning-Distilled
- 基础模型: https://huggingface.co/Qwen/Qwen3.5-27B
