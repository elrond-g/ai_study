# LangSmith

> https://www.langchain.com/langsmith

## 项目简介

LangSmith 是 LangChain 团队推出的 LLM 应用可观测性与评测平台，覆盖从开发调试到生产监控的全生命周期。分为 Observability（可观测性）和 Evaluation（评测）两大模块，是构建生产级 LLM 应用的核心基础设施。

## Observability（可观测性）

**核心能力：**
- **全链路追踪**：记录每次 LLM 调用的输入/输出、延迟、token 用量
- **链式调用可视化**：图形化展示 Chain、Agent 的执行路径
- **错误诊断**：快速定位失败节点和异常输入
- **实时监控**：生产环境下的 LLM 调用监控和告警

地址：https://www.langchain.com/langsmith/observability

## Evaluation（评测）

**核心能力：**
- **数据集管理**：创建和管理测试用例集
- **自动评测**：LLM-as-Judge，让模型评估模型输出质量
- **回归测试**：对比新旧模型版本的性能差异
- **人工标注**：集成人工标注流程，构建高质量评测数据

地址：https://www.langchain.com/langsmith/evaluation

## 技术特点

- 与 LangChain 深度集成，几行代码即可接入
- 支持非 LangChain 项目，可通过 SDK 独立使用
- 提供免费 tier，适合个人开发者

## 快速开始

```python
import os
os.environ["LANGCHAIN_TRACING_V2"] = "true"
os.environ["LANGCHAIN_API_KEY"] = "your-api-key"
# 之后所有 LangChain 调用自动被追踪
```

## 相关链接

- Observability: https://www.langchain.com/langsmith/observability
- Evaluation: https://www.langchain.com/langsmith/evaluation
