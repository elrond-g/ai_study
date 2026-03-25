# Unsloth

> ⭐ 25k+ | Python | https://github.com/unslothai/unsloth

## 项目简介

2-5 倍加速 LLM 微调，降低 70% 显存占用，支持 Llama、Mistral、Qwen 等主流模型。让消费级显卡也能微调大模型。

## 核心功能

- **极速微调**：通过手写反向传播内核，实现 2-5 倍训练加速且无精度损失
- **显存优化**：70% 显存占用降低，单张 24GB 显卡即可微调 70B 参数模型
- **广泛模型支持**：兼容 Llama 3、Mistral、Qwen 2、Gemma、Phi 等主流架构

## 技术特点

- 手写 Triton 内核替代标准实现，从底层优化计算效率
- 完全兼容 Hugging Face 生态与 PEFT/LoRA 工作流
- 支持导出为 GGUF / vLLM / Ollama 等推理格式

## 使用场景

- 在消费级 GPU 上微调大参数模型
- 低成本快速迭代领域专用模型
- 结合 Ollama 部署本地微调后的自定义模型

## 相关链接

- GitHub: https://github.com/unslothai/unsloth
