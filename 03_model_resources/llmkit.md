# llmkit

> ⭐ 119 | Rust | https://github.com/llmkit-ai/llmkit

## 项目简介

llmkit 是一个提供商无关的 LLM 性能工具集，集成了 Prompt 管理、版本控制、测试和评测功能的推理服务器及 UI 工具包。适合需要系统化管理 Prompt 工程工作流的开发团队。

## 核心功能

- **Prompt 版本管理**：像 Git 一样管理 Prompt 的迭代历史
- **A/B 测试**：对比不同 Prompt 版本在相同输入下的输出差异
- **评测框架**：批量运行测试用例，量化 Prompt 质量
- **推理服务器**：统一的 API 服务层，兼容 OpenAI 格式
- **UI 工具包**：可视化界面管理 Prompt 和测试结果

## 技术特点

- Rust 实现，高性能低延迟
- 提供商无关（Provider-agnostic），支持任意 LLM 后端
- OpenAI API 兼容，现有代码无需修改

## 使用场景

- 团队协作管理 Prompt，追踪版本演进
- 系统化测试 Prompt 修改对输出质量的影响
- 构建内部 LLM 服务层，统一管理模型调用

## 相关链接

- GitHub: https://github.com/llmkit-ai/llmkit
