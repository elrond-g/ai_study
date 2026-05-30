# Knowledge Work Plugins

Anthropic 开源的知识工作者插件集，为 Claude Cowork 和 Claude Code 提供角色专属能力。包含 11 个针对不同职能的插件：生产力、销售、客服、产品管理、市场营销、法务、财务、数据分析、企业搜索等。

## 核心特性

### 11 个专业角色插件
| 插件 | 定位 | 集成 |
|------|------|------|
| productivity | 任务/日历/工作流管理 | Slack, Notion, Asana, Linear, Jira |
| sales | 客户研究/外展/竞争分析 | Slack, HubSpot, Close, Clay, ZoomInfo |
| customer-support | 工单分类/回复/知识库 | Slack, Intercom, HubSpot, Guru, Jira |
| product-management | 规格/路线图/用户研究 | Slack, Linear, Figma, Amplitude, Pendo |
| marketing | 内容/活动/品牌/报告 | Slack, Canva, Figma, HubSpot, Ahrefs |
| legal | 合同审查/NDA/合规 | Slack, Box, Egnyte, Jira |
| finance | 分录/对账/报表/审计 | Snowflake, Databricks, BigQuery, Slack |
| data | 查询/可视化/统计分析 | Snowflake, Databricks, BigQuery, Hex |
| enterprise-search | 跨系统统一搜索 | 邮件/聊天/文档/Wiki |

### 可定制化
每个插件可针对企业工具、术语、流程进行定制，让 Claude 像为团队量身打造。

### 双平台兼容
同时兼容 Claude Cowork（知识工作者助手）和 Claude Code（开发者工具）。

## 技术架构

- **平台**：Claude Cowork + Claude Code
- **结构**：每个插件 = Skills + Connectors + Slash Commands + Sub-agents
- **集成**：40+ 企业 SaaS 工具

## 安装与使用

Claude Cowork 中直接启用对应插件。

## GitHub

https://github.com/anthropics/knowledge-work-plugins
