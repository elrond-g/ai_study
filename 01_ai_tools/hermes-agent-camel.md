# Hermes Agent + CaMeL

> ⭐ 77 | MIT | https://github.com/nativ3ai/hermes-agent-camel

## 项目简介

Hermes Agent 的安全强化分支，将 Google Research 提出的 CaMeL（Capabilities Model）信任边界机制融合进 Hermes 运行时，以防御来自不可信数据源的间接提示注入攻击。

## 核心安全特性

- **信任层分离**：区分受信任的 operator 控制流 vs 不可信的工具输出
- **用户 Turn 计划提取**：只从真实用户输入提取执行计划
- **能力门控（Capability Gating）**：对敏感操作（终端命令、文件修改、消息发送）强制授权检查
- **三种运行时模式**：
  - `guarded`：严格执行 CaMeL 策略
  - `monitoring`：只监控不拦截
  - `legacy`：禁用防护（向后兼容）
- **来源感知数据包装**：外部数据携带 Provenance 标签

## 技术栈

- Python Agent 框架
- 依赖 mini-swe-agent + tinker-atropos（子模块）
- 改编自 NousResearch 的 Hermes Agent

## 为什么值得关注

- 将学术 CaMeL 论文的核心思想落地到实际 Agent 运行时
- 关注 Agent 安全的工程实践参考
- 对构建生产级 Agent 必读——间接 Prompt Injection 是 OWASP Agentic Top 10 重点问题

## 相关链接

- GitHub: https://github.com/nativ3ai/hermes-agent-camel
- CaMeL 原论文：Google Research 出品
