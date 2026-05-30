# Agent Governance Toolkit

微软出品的 AI Agent 治理工具包。覆盖策略执行、零信任身份、执行沙箱和可靠性工程四大领域，覆盖 OWASP Agentic Top 10 全部 10 项风险。支持 Python（pip）、TypeScript（npm）、C#（NuGet）。

## 核心特性

### 策略执行
定义 Agent 可执行操作的细粒度策略——有 send_email 和 query_database 权限的 Agent 不应能执行 drop_table。

### 零信任身份
多 Agent 系统中，即使共享 API Key，也能追踪每个具体 Agent 的操作，实现操作级归属。

### 执行沙箱
为 Agent 的工具调用提供安全隔离的执行环境，防止越权操作。

### 可审计性
提供防篡改的操作审计日志，满足合规和监管要求。

### OWASP 全覆盖
覆盖 OWASP Agentic Top 10 全部 10 项安全风险。

## 技术架构

- **语言支持**：Python（PyPI）、TypeScript（npm）、C#（NuGet）
- **许可**：MIT
- **框架无关**：与具体 Agent 框架解耦

## 安装与使用

```bash
pip install agent-governance-toolkit
```

## GitHub

https://github.com/microsoft/agent-governance-toolkit
