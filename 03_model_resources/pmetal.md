# pmetal（Powdered Metal）

> ⭐ 182 | Rust | https://github.com/Epistates/pmetal | https://pmetal.io

## 项目简介

pmetal（Powdered Metal）是专为 Apple Silicon 设计的高性能 LLM 一体化框架，在 macOS 上统一提供模型训练、强化学习（RL）和推理能力。利用苹果 Metal GPU 和统一内存架构，在 Mac 硬件上实现接近服务器级的 LLM 工作流。

## 核心功能

- **模型训练**：在 Apple Silicon 上直接进行 LLM 微调训练
- **强化学习**：支持 RLHF 等强化学习流程
- **高效推理**：Metal 加速推理，充分利用统一内存
- **TUI 界面**：终端用户界面，直观监控训练进度

## 技术特点

- Rust 实现，性能极致，内存安全
- 基于 Apple Metal GPU 和 MLX 框架
- ANE（Apple Neural Engine）加速支持
- 支持模型知识蒸馏（Distillation）

## 为什么值得关注

Mac M 系列芯片的统一内存架构（CPU/GPU 共享内存）天然适合大模型——M3 Max/M4 Max 可拥有 128GB 统一内存，比大多数消费级 GPU 显存大数倍。pmetal 是充分利用这一优势的工具之一。

## 使用场景

- Mac 用户在本地进行小规模 LLM 微调实验
- 研究者在 Apple Silicon 上探索强化学习对齐
- 边缘部署场景的模型优化和推理

## 相关链接

- GitHub: https://github.com/Epistates/pmetal
- 官网: https://pmetal.io
