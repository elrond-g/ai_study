# OmniVoice

> GitHub | https://github.com/k2-fsa/OmniVoice

## 项目简介

OmniVoice 是一个支持 600+ 语言的零样本多语言 TTS（文本转语音）模型，基于新型扩散语言模型架构构建，支持语音克隆和语音设计，推理速度极快（RTF 低至 0.025，40 倍实时速度）。

## 核心特点

- **600+ 语言支持**：零样本 TTS 模型中最广泛的语言覆盖
- **语音克隆**：SOTA 级别的语音克隆质量
- **语音设计**：通过属性控制语音（性别、年龄、音调、方言/口音、耳语等）
- **极速推理**：RTF 低至 0.025（40 倍实时速度）
- **扩散语言模型架构**：简洁、流线型、可扩展的设计

## 安装

```bash
# PyPI
pip install omnivoice

# 从源码
git clone https://github.com/k2-fsa/OmniVoice.git
cd OmniVoice
pip install -e .

# uv
uv sync
```

## 快速使用

```bash
# 启动本地 Web UI
omnivoice-demo --ip 0.0.0.0 --port 8001
```

支持 NVIDIA GPU 和 Apple Silicon。

## 技术规格

- **语言**：Python
- **Stars**：600+
- **架构**：Diffusion Language Model
- **平台**：NVIDIA GPU / Apple Silicon

## 相关链接

- GitHub: https://github.com/k2-fsa/OmniVoice
- HuggingFace Model: https://huggingface.co/k2-fsa/OmniVoice
- HuggingFace Space: https://huggingface.co/spaces/k2-fsa/OmniVoice
- 论文: https://arxiv.org/abs/2604.00688
