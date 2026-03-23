# TorchCode

> https://github.com/duoan/TorchCode

## 项目简介

TorchCode 是一个手写 PyTorch 算子实现的学习项目，通过从零实现各类深度学习算子（操作符），深入理解神经网络底层计算原理。与 CS336 的思路类似，通过"手扒"经典实现来真正掌握 AI 基础设施。

## 涵盖的算子实现

**基础算子：**
- 矩阵乘法（包含 CUDA 优化版本）
- Softmax（数值稳定版本）
- Layer Normalization / RMS Norm
- Dropout

**Attention 相关：**
- Scaled Dot-Product Attention
- Multi-Head Attention
- Flash Attention 原理实现

**激活函数：**
- GELU、SiLU、ReLU 及其变体

**优化器：**
- SGD、Adam、AdamW 手写实现

## 学习价值

理解算子实现的三层意义：
1. **数学层**：理解背后的数学公式
2. **计算层**：理解数值稳定性和计算效率
3. **硬件层**：理解 GPU 并行计算和内存访问模式

## 适合人群

- 希望深入理解 PyTorch 底层的开发者
- AI 系统工程师（MLE/AI Infra）的进阶学习
- 准备 AI 公司技术面试的候选人

## 相关链接

- GitHub: https://github.com/duoan/TorchCode
