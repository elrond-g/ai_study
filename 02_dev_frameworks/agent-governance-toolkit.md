# Agent Governance Toolkit

> GitHub | https://github.com/microsoft/agent-governance-toolkit

## 项目简介

微软开源的 AI Agent 治理工具包，提供运行时治理基础设施——确定性策略执行、零信任身份、执行沙盒和可靠性工程。覆盖 OWASP Agentic Top 10 全部 10 项风险，9,500+ 测试用例。支持 Python/TypeScript/.NET/Rust/Go 五种语言 SDK。

## 核心定位

> **治理 Agent 的行为（工具调用、资源访问、Agent 间通信），而非模型输出内容。**

不是模型安全或 Prompt 护栏工具，不过滤 LLM 输入/输出，而是在应用层治理 Agent 的实际操作。

## 核心功能

### 确定性策略执行
- 每个 Agent 操作在执行前经过策略评估，亚毫秒延迟（<0.1ms）

### 零信任 Agent 身份
- Ed25519 加密凭证
- SPIFFE/SVID 支持
- 0-1000 信任评分

### 执行沙盒
- 4 层特权环
- Saga 编排
- 终止控制 + Kill Switch

### Agent SRE
- SLO、错误预算
- 回放调试
- 混沌工程、熔断器
- 渐进式发布

### MCP 安全扫描器
- 检测工具投毒、Typosquatting、隐藏指令、Rug-pull 攻击

## 框架集成

兼容 12+ 框架：LangChain、CrewAI、AutoGen、Dify、LlamaIndex、OpenAI Agents、Google ADK、Azure AI 等。纯 `pip install` 零厂商锁定。

## 安装

```bash
# Python
pip install agent-governance-toolkit[full]

# TypeScript
npm install @agentmesh/sdk

# .NET
dotnet add package Microsoft.AgentGovernance
```

## OWASP Agentic Top 10 覆盖

10/10 全覆盖，ASI-01 到 ASI-10 每项风险都有专门控制。

## 技术规格

- **语言**：Python / TypeScript / .NET / Rust / Go
- **Stars**：450+
- **许可证**：MIT
- **测试**：9,500+

## 相关链接

- GitHub: https://github.com/microsoft/agent-governance-toolkit
- OWASP 合规: https://github.com/microsoft/agent-governance-toolkit/blob/main/docs/OWASP-COMPLIANCE.md
- 架构文档: https://github.com/microsoft/agent-governance-toolkit/blob/main/docs/ARCHITECTURE.md
