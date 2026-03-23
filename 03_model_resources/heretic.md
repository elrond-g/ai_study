# heretic

> ⭐ 16,498 | Python | https://github.com/p-e-w/heretic

## 项目简介

heretic 是一个全自动移除语言模型安全审查（Censorship）的工具，基于"Abliteration"技术——通过直接修改模型权重中的拒绝方向向量，而不是微调，永久性地移除模型的拒绝行为。

## 核心技术：Abliteration

传统方法通过微调训练覆盖安全行为，而 Abliteration 采用更直接的方式：

1. 收集模型对拒绝和合规两类 prompt 的中间层激活
2. 计算两类激活的"拒绝方向"向量
3. 从模型权重矩阵中减去该方向，永久移除拒绝倾向

相比微调，这种方法更彻底、更快速，无需训练数据集。

## 技术特点

- Python 实现，依赖 Transformers 和 PyTorch
- 支持任意 HuggingFace 格式的开源模型
- 处理后的模型可直接导出为标准格式

## 注意事项

heretic 是研究性工具，展示了 LLM 安全机制的工作原理及其脆弱性。了解这类技术有助于：
- 理解当前 RLHF 安全对齐的局限性
- 研究更鲁棒的安全对齐方法
- 评估自部署开源模型的风险

## 相关链接

- GitHub: https://github.com/p-e-w/heretic
