# LiteLLM

> ⭐ 40,000+ | Python | https://github.com/BerriAI/litellm | https://docs.litellm.ai/docs/

## 项目简介

LiteLLM 是一个统一多模型接口的 Python SDK 和 AI 网关代理服务器，用一套 OpenAI 格式的 API 调用 100+ 个 LLM 提供商。无论是 Claude、GPT、Gemini、Llama 还是 Mistral，代码完全相同，只需切换模型名即可。

## 核心功能

- **100+ 模型统一接口**：Bedrock、Azure OpenAI、Anthropic、VertexAI、Cohere、HuggingFace、VLLM 等全覆盖
- **AI Gateway 代理**：可部署为代理服务器，集中管理所有 LLM 调用
- **成本追踪**：实时统计各模型的 token 用量和费用
- **负载均衡**：多个 API Key 和模型端点间自动负载均衡
- **Guardrails**：内容安全过滤和输出格式约束
- **完整日志**：对接 Langfuse、Helicone 等可观测性平台

## 技术特点

- 与 OpenAI Python SDK 100% 兼容，迁移成本极低
- 支持同步和异步调用
- 内置重试和回退机制

## 快速开始

```python
from litellm import completion

response = completion(
    model="claude-sonnet-4-6",
    messages=[{"role": "user", "content": "Hello"}]
)
```

## 相关链接

- GitHub: https://github.com/BerriAI/litellm
- 文档: https://docs.litellm.ai/docs/
