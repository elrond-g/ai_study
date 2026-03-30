# awesome-harness-engineering

> Walking Labs | 精选列表 | https://github.com/walkinglabs/awesome-harness-engineering

## 项目简介

Harness Engineering（代理工程）领域的精选资源库，汇集文章、指南、基准测试、规范和开源项目。核心理念：**Model + Harness = Agent**——弱代理结果通常是代理系统问题而非模型问题。

## 核心概念

Harness Engineering 是围绕 AI Agent 构建环境的学科：提示、工具、中间件、编排和运行时基础设施。目标是让 Agent 在生产环境中可靠工作。

## 收录内容分类

### 概念框架
- Thoughtworks：上下文工程、架构约束、熵的"垃圾回收"
- Anthropic：工作流、Agent、工具和结构化系统指南
- OpenAI、LangChain 等行业领导者技术文章

### 实践工具
- **Inngest**：TypeScript 工具包，事件驱动的持久化 Agent 工作流
- **Harbor**：大规模 Agent 评估和改进系统
- **Terminal-Bench**：Shell 原生 Agent 评估基准

### 评估基准
- **HAL**：综合 Agent 排行榜，关注可靠性/成本/覆盖广度
- **OSWorld**：369 个跨 Ubuntu/Windows/macOS 的真实任务基准

### 规范标准
- **AGENTS.md**：开源、工具无关的 Agent 项目指令格式，已成为 Agentic AI Foundation 开放标准
- 支持分层嵌套指令文件

## 关键技术维度

- 多 Agent 系统设计（规划器、编码器、评估器）
- 约束与监控（代码检查器、结构化测试、品味不变量）
- 安全保障（权限模型、默认只读、自动快照、预提交 Hooks）
- 反馈循环（测试-修复自动验证）

## 为什么值得关注

弥合 AI 模型能力和生产可靠性之间的鸿沟。整合了 Anthropic、Thoughtworks、OpenAI 等行业最佳实践，是 Agent 系统工程化的权威参考。

## 相关链接

- GitHub: https://github.com/walkinglabs/awesome-harness-engineering
- Martin Fowler 文章: https://martinfowler.com/articles/exploring-gen-ai/harness-engineering.html
- Anthropic Harness 设计: https://www.anthropic.com/engineering/harness-design-long-running-apps
