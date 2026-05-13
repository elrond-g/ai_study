# Understand-Anything

将任意代码库、知识库或文档转化为交互式知识图谱的 Claude Code Plugin。多 Agent 流水线分析项目结构（文件/函数/类/依赖），构建可视化知识图谱，支持跨平台（Claude Code / Codex / Cursor / Copilot / Gemini CLI / Hermes 等）。

## 核心特性

### 代码结构图谱
交互式知识图谱展示每个文件、函数、类作为节点，支持点击查看摘要、依赖关系和引导式学习路径。图布局：75% 画布 + 360px 侧边栏，暗色豪华主题（#0a0a0a / #d4a574 金色点缀），React Flow + Zustand + TailwindCSS v4。

### 多 Agent 流水线
7 个专业化 Agent 协作：
- `project-scanner` — 发现文件、检测语言和框架
- `file-analyzer` — 提取函数/类/导入，生成图节点和边
- `architecture-analyzer` — 识别架构层次
- `tour-builder` — 生成引导式学习路径
- `graph-reviewer` — 验证图谱完整性和引用完整性
- `domain-analyzer` — 提取业务领域/流程/步骤
- `article-analyzer` — 从 Wiki 文章提取实体/论断/隐式关系

文件分析 Agent 并行运行（最多 5 个并发，每批 20-30 文件），支持增量更新。

### 架构层次自动分层
自动按 API / Service / Data / UI / Utility 分层着色，带图例。

### 变更影响分析
`/understand-diff` — 提交前查看代码变更对系统的影响范围和连锁反应。

### 知识库分析
`/understand-knowledge` — 分析 Karpathy 模式的 LLM Wiki，生成力导向知识图谱，提取 wikilinks、社区聚类和隐式关系。

### 跨平台支持

| 平台 | 安装方式 |
|------|---------|
| Claude Code | `/plugin marketplace add Lum1104/Understand-Anything` |
| Codex / OpenCode / Hermes / Gemini CLI / Cline 等 | `curl -fsSL .../install.sh \| bash` |
| Cursor / VS Code Copilot | 克隆仓库自动发现 |
| Copilot CLI | `copilot plugin install Lum1104/Understand-Anything:understand-anything-plugin` |

## 技术架构

- **Monorepo**（pnpm workspace）
- **核心包**：`@understand-anything/core`（分析引擎：类型/持久化/tree-sitter/搜索/schema）
- **仪表盘**：`@understand-anything/dashboard`（React + TypeScript）
- **插件**：`understand-anything-plugin`（Claude Code / 多平台适配）
- **代码解析**：web-tree-sitter（WASM），避免原生 tree-sitter 在 darwin/arm64 + Node 24 的兼容问题
- **TypeScript strict mode**，ESM 模块，Vitest 测试

## 安装与使用

```bash
# Claude Code
/plugin marketplace add Lum1104/Understand-Anything
/plugin install understand-anything

# 分析代码库
/understand

# 打开可视化仪表盘
/understand-dashboard

# 对话式查询
/understand-chat 支付流程是怎么工作的？

# 变更影响分析
/understand-diff

# 单文件深度分析
/understand-explain src/auth/login.ts

# 生成新人入职指南
/understand-onboard

# 业务领域分析
/understand-domain
```

## 知识图谱共享

图谱是纯 JSON——提交到仓库后团队成员无需重新运行流水线即可使用。大型图谱（>10MB）建议用 git-lfs 管理。

## GitHub

https://github.com/Lum1104/Understand-Anything
