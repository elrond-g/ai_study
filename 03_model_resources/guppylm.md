# GuppyLM

> ⭐ 3k | MIT | https://github.com/arman-bd/guppylm

## 项目简介

"训练 LLM 并不神秘"——GuppyLM 是一个 9M 参数的超小型语言模型，以小鱼视角回答问题（关于食物、水温、气泡等），核心目标是降低 LLM 训练的心智门槛，让任何人都能复现一次完整的训练流程。

## 关键特性

- **模型规模**：~9M 参数，Vanilla Transformer 架构
- **训练数据**：60 个主题 × 合成对话，共 60K 样本
- **训练时间**：单 GPU 约 5 分钟
- **上下文窗口**：128 tokens
- **部署方式**：可通过 WebAssembly 在浏览器运行
- **导出格式**：支持 ONNX

## 技术栈

- Python + PyTorch
- Transformers + BPE Tokenizer
- ONNX 导出 + WASM 浏览器部署

## 为什么值得关注

与 MiniMind 类似但更极致：GuppyLM 将"训练 LLM"压缩到 5 分钟单 GPU 的极限体验。对想快速理解 LLM 全链路训练的人来说是最佳入门项目——从数据合成、训练、量化到浏览器部署全流程复现。

## 相关链接

- GitHub: https://github.com/arman-bd/guppylm
