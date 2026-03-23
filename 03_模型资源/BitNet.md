# BitNet

> ⭐ 36,410 | Python | https://github.com/microsoft/BitNet

## 项目简介

BitNet 是微软研究院开源的 1-bit LLM 官方推理框架，专为运行 1-bit 量化的大语言模型而设计。1-bit LLM（BitNet b1.58）将模型权重压缩到每个参数仅 1.58 bit，在大幅降低内存和计算需求的同时保持接近全精度的性能。

## 核心技术

**1-bit 量化原理：**
- 传统 FP16 模型每个权重 16 bit
- BitNet b1.58 每个权重只需 1.58 bit（值域：-1, 0, +1）
- 矩阵乘法变为加法运算，CPU 可高效执行

**性能提升：**
- 相比 FP16，内存占用降低 **8-10x**
- 推理速度提升 **2-4x**（CPU 上）
- 能耗大幅降低

## 技术特点

- CPU 推理深度优化，不依赖高端 GPU 即可运行
- 支持 Apple Silicon、x86 等多种 CPU 架构
- 提供预训练 BitNet 模型（1B、3B、8B 等规模）

## 快速开始

```bash
git clone --recursive https://github.com/microsoft/BitNet
pip install -r requirements.txt
# 参考 README 下载预训练模型后运行推理
```

## 使用场景

- 在 CPU/边缘设备上运行 LLM（树莓派、笔记本等）
- 降低 LLM 部署的硬件门槛和运营成本
- 研究极致压缩下的模型能力边界

## 相关链接

- GitHub: https://github.com/microsoft/BitNet
