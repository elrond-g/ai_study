# Lucebox Hub

> ⭐ 800+ | C++ / CUDA | https://github.com/Luce-Org/lucebox-hub | https://lucebox.com

## 项目简介

Lucebox 的开源 LLM 推理优化中心，"为特定芯片手工重写 LLM 推理"——不等新硬件，专门为某一款消费级 GPU（如 RTX 3090）手工调优内核、投机解码和量化方案，每个子项目配独立 Benchmark 和论文级写作。

## 核心功能

- **Megakernel**：Qwen3.5-0.8B 24 层融合进单次 CUDA dispatch，RTX 3090 上 1.87 tok/J，与 Apple 最新芯片能效持平但吞吐量 2 倍
- **DFlash DDTree**：Qwen3.5-27B GGUF 投机解码首个移植版，Q4_K_M + BF16 draft，207 tok/s 峰值、HumanEval 均值 129.5 tok/s，比自回归快 3.43×
- **128K 上下文 / 24GB**：Q4_0 KV 缓存 + 滑动 target_feat 环形缓冲，单张 3090 即可跑 128K 上下文

## 技术特点

- 82 blocks × 512 threads 的持久化内核，层间无 CPU 往返，权重直接从 HuggingFace 流式载入
- 自研三个 tree-aware SSM 状态回滚 CUDA kernel（`ggml_ssm_conv_tree` 等），绕开 libllama 直接基于 ggml
- 功耗墙先于计算墙触发，DVFS 将紧凑执行直接转换为节省的瓦特（220W 最优点）

## 使用场景

- 消费级 GPU 本地部署大模型，榨干硬件潜力
- 研究投机解码 / megakernel / GGUF 量化等推理优化技术
- 对比主流推理引擎（llama.cpp、SGLang、vLLM）的性能天花板

## 相关链接

- GitHub: https://github.com/Luce-Org/lucebox-hub
- 官网: https://lucebox.com
- 博客: https://lucebox.com/blog
