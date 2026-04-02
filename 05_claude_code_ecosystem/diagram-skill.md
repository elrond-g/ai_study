# Diagram Skill（画图技能）

> GitHub | https://github.com/312362115/claude/blob/main/skills/diagram/SKILL.md

## 项目简介

专业的 Claude Code 图表生成 Skill，支持 29 种图表类型，输入自然语言描述即可自动选择合适的图表类型并生成符合设计规范的 PNG 图表。统一使用 HTML/SVG + 内联 JS 布局计算，ER/类图使用 ELKjs 布局引擎。

## 支持的图表类型

### 结构图（17 种）

| 图表 | 用途 |
|------|------|
| 流程图（线性/DAG） | 工作流程、决策逻辑、资源流转 |
| 泳道图 | 多角色协作流程 |
| 时序图 | API 调用、消息交互 |
| 架构图 | 系统分层、技术栈 |
| ER 图 | 数据库表结构 |
| 类图 | 面向对象设计 |
| 状态图 | 状态迁移 |
| 网络图 | 网络拓扑 |
| 决策树 | 选型决策 |
| 数据流图 | 数据管道 |
| C4 图 | C4 系统视图 |
| 思维导图 | 知识结构 |
| 甘特图 | 项目排期 |
| 时间线 | 发展历程 |
| 组织结构图 | 组织架构 |
| Kanban | 项目管理/任务看板 |
| Git Graph | Git 分支工作流 |

### 统计图（12 种）

柱状图、折线图、饼图、雷达图、热力图、散点图、桑基图、矩形树图、柱线混合图、SWOT 图、鱼骨图、文氏图

## 技术特点

- **三种输出格式**：PNG（默认）、HTML（富文档嵌入）、DSL（Mermaid 文本）
- **统一设计规范**：所有图表遵循统一配色/字体/组件/间距，风格现代简洁
- **Mermaid/Graphviz 转换**：自动识别 `mermaid` 和 `dot` 代码块，解读图结构后用统一规范渲染
- **ELKjs 布局引擎**：ER 图、类图、DAG 流程图使用 ELKjs 自动布局
- **触发词**：画图、画一个、生成图表、流程图、架构图、时序图、柱状图等

## 规范体系

- `references/design-system.md` — 公共配色、字体、组件、间距
- `references/diagram-utils.md` — SVG 工具函数、文字测量、碰撞检测
- `references/diagrams/<type>.md` — 每种图表的数据结构、布局规则、渲染细节

## 相关链接

- SKILL.md: https://github.com/312362115/claude/blob/main/skills/diagram/SKILL.md
