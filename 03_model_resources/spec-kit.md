# Spec Kit

> ⭐ GitHub 官方 | Python CLI + Markdown 模板 | https://github.com/github/spec-kit | https://speckit.org

## 项目简介

Spec Kit 是 GitHub 官方开源的 **Spec-Driven Development（SDD，规范驱动开发）** 工具集。核心理念是"先写规范、再让 AI 生成代码"——把 PRD（产品需求文档）作为生成实现的源头，而非事后补写的文档。工具包含 Specify CLI 和一套跨 Agent 兼容的模板体系，支持 GitHub Copilot、Claude Code、Gemini CLI 等主流 AI 编码助手。

## 核心概念

### Spec-Driven Development（SDD）

传统开发：先写代码 → 再补文档。SDD 反转这个流程：

1. 先写规范（Spec）作为唯一真相源
2. 规范生成技术计划
3. 技术计划分解为可执行任务
4. AI Agent 按任务逐个实现

规范不是给人看的参考文档，而是给 AI Agent 的生成指令。

### Constitution（宪法文件）

引入 `constitution.md`，定义项目不可违反的原则（测试策略、技术栈约定、架构风格等）。所有 SDD 迭代都受其约束，适合团队/组织统一技术标准。

## 两大组件

### 1. Specify CLI

Python 编写的命令行工具，一条命令初始化 SDD 项目：

```bash
uvx --from git+https://github.com/github/spec-kit.git specify init <PROJECT_NAME>
```

自动下载适配当前 Agent 的官方模板，跨 Agent 兼容。

### 2. 模板与辅助脚本

定义了规范、技术计划、任务分解的标准格式，以及各阶段的检查点。

## 四阶段工作流

| 阶段 | 命令 | 说明 |
|------|------|------|
| 宪法 | `/constitution` | 建立项目不可违反的原则 |
| 规范 | `/specify` | 从高层 prompt 生成完整规范（PRD） |
| 计划 | `/plan` | 从规范生成技术实现方案 |
| 任务 | `/tasks` | 分解为可执行的任务清单 |
| 实现 | `/implement` | AI Agent 按任务逐个执行 |

每个阶段有明确的检查点（checkpoint），人类在关键节点审核把关，AI 做大部分编写工作。

## 技术特点

- **跨 Agent 兼容**：模板设计兼容 Copilot、Claude Code、Gemini CLI 等，无需为不同工具定制
- **Python CLI**：基于 `uv` 生态，安装和使用极简
- **社区扩展**：`catalog.community.json` 收录社区贡献的扩展（多 Agent 工作流、Jira 集成、漂移检测等）
- **宪法机制**：组织级技术标准的统一管控

## 为什么值得关注

1. **GitHub 官方出品**：代表 GitHub 对 AI 辅助开发流程的官方思考
2. **方法论 + 工具**：不仅提供工具，更定义了一套完整的 AI 辅助开发方法论
3. **解决 AI 编码核心痛点**：AI 生成代码时最大问题是"不知道你要什么"，SDD 通过规范前置彻底解决
4. **团队协作友好**：Constitution + Spec 机制让团队能统一管控 AI 编码输出的质量和风格

## 使用场景

- 团队项目中用 AI Agent 开发新功能前，先定义清晰规范
- 组织级统一 AI 编码标准（通过 Constitution 约束）
- 复杂功能的渐进式实现：规范 → 计划 → 任务 → 实现
- 跨 Agent 工具的标准化开发流程

## 相关链接

- GitHub: https://github.com/github/spec-kit
- 官网: https://speckit.org
- 博客: https://github.blog/ai-and-ml/generative-ai/spec-driven-development-with-ai-get-started-with-a-new-open-source-toolkit/
- 微软开发者博客: https://developer.microsoft.com/blog/spec-driven-development-spec-kit
