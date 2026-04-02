# AI 工程的真实代价：从 Claude Code 泄露源码看新模型接入的工程现实

> 鸭哥每日手记 | https://yage.ai/share/claude-code-engineering-cost-20260331.html

## 文章简介

深度分析 Claude Code 泄露的 512,000 行 TypeScript 源码，还原 AI 工程中将新模型（内部代号 Capybara）接入成熟 Agentic 系统的真实工程代价。不同于安全漏洞视角，本文聚焦工程细节。

## 核心内容

### 1. 反蒸馏：三层技术防线

| 层级 | 机制 | 目的 |
|------|------|------|
| Fake Tools 注入 | API 响应中注入虚假工具调用 | 污染训练数据集 |
| Connector Text Summarization | 模型推理文本替换为加密签名摘要 | 遮蔽推理过程细节 |
| Token-Efficient Tools (FC v3) | JSON 格式工具调用协议 + v2 Header | 协议层流量隔离 |

三层各自独立开关，通过 GrowthBook 灰度部署，纵深防御思路。

### 2. 缓存保卫战：50,000 Token 的代价

- Prompt Caching 是成本和延迟的关键优化，但几乎任何参数变化都会打破缓存
- 发明 **sticky-on latch** 机制：beta header 一旦首次发送就永不移除，避免破坏 50-70K token 缓存
- 功能状态和协议状态有意解耦：header（协议层）保持不变，功能控制在 body 层动态调整
- 77% 的工具相关缓存失效来自工具描述变化（AgentTool/SkillTool 嵌入动态列表）

### 3. SDK 的尴尬与流式解析脱钩

- Anthropic 旗舰产品因性能原因绕过了自家 SDK
- SDK 的 BetaMessageStream 在每个 delta 事件上做 O(n²) partialParse
- Claude Code 重写了流式解析，自己处理文本累积、thinking block 签名拼接

### 4. 模型行为的五个工程故事

| 问题 | 根因 | 修复 |
|------|------|------|
| 空工具结果导致零输出 | 空 tool_result 被模型误判为 turn boundary | 注入 `(toolName completed with no output)` |
| tool_reference 展开触发假结束 | `<functions>` 标签与系统 prompt 格式相同，10.5% 触发 stop | 迁移文本 sibling 到下一条消息 |
| 模型回退时签名不兼容 | Thinking block 签名与模型/API key 绑定 | 回退前 stripSignatureBlocks |
| 虚假成功报告率翻倍 | Capybara v8 FC rate 29-30%（v4 为 16.7%） | 系统 prompt 注入诚实报告指令 |
| 安全分类器被 alwaysOnThinking 噎死 | Capybara 拒绝关闭 thinking，耗尽分类器 token | 给 max_tokens 加 2048 headroom |

### 5. Undercover 模式

- Anthropic 工程师用 Claude Code 贡献开源代码时启用
- 隐藏模型代号（Capybara、Tengu 等），防止在 commit message 和 PR 中泄露
- 只有 force-ON 没有 force-OFF，17 个内部白名单仓库才关闭

## 核心洞察

> 新模型接入的工程成本中，大部分来自模型行为与系统假设之间的不匹配。模型能力在快速进步，把这些能力接入生产系统的成本以完全不同的速率在增长。

## 相关链接

- 原文: https://yage.ai/share/claude-code-engineering-cost-20260331.html
