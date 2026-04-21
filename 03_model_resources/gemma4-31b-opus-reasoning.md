# Gemma4-31B-Opus-4.6-Reasoning

> HuggingFace | Apache 2.0 | https://huggingface.co/kai-os/gemma4-31b-Opus-4.6-reasoning

## 项目简介

基于 Google `gemma-4-31B-it` 基础模型，使用 QLoRA 微调 2,025 条清洗后的 Opus-4.6-Reasoning 样本（1,899 数学 + 126 代码）得到的推理能力增强 Adapter。将 Claude Opus 4.6 的链式思维风格蒸馏到 Gemma 4 家族。

## 训练细节

- **基础模型**：google/gemma-4-31B-it（31B 参数）
- **训练方法**：QLoRA + 4-bit NF4 量化 + BF16 计算
- **训练数据**：2,025 条 Opus-4.6 推理样本（数学为主，少量代码）
- **训练轮次**：2 epochs
- **硬件**：NVIDIA GH200
- **评估困惑度**：36.66

## 使用方式

PEFT LoRA Adapter，不是独立模型，需要与基础模型联合加载：

```python
from peft import PeftModel
from transformers import AutoModelForCausalLM

base = AutoModelForCausalLM.from_pretrained("google/gemma-4-31B-it", load_in_4bit=True)
model = PeftModel.from_pretrained(base, "kai-os/gemma4-31b-Opus-4.6-reasoning")
```

## 特点

- 专注数学和代码推理场景，Opus 风格 CoT 输出格式
- 4-bit 量化后消费级显卡可部署
- 非 benchmark 优化版本，定位为实验性蒸馏 Adapter
- Apache 2.0 许可，商用友好

## 相关链接

- HuggingFace: https://huggingface.co/kai-os/gemma4-31b-Opus-4.6-reasoning
- 基础模型: https://huggingface.co/google/gemma-4-31B-it
