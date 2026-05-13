# Oz Skills

Warp 官方维护的 Agent Skills 精选目录，遵循 [Agent Skills](https://agentskills.io) 开放标准。面向 Warp AI Agent 和 Oz 的可复用技能集合，用户可直接复制到项目中使用。

## 核心特性

### Agent Skills 标准
每个 Skill 是一个包含 `SKILL.md` 的文件夹，含 YAML frontmatter 和 Markdown 指令。Agent 自动发现并加载相关 Skill。
- `name` — kebab-case 标识符
- `description` — 两句：祈使动词摘要 + `Use when...` 触发条件
- 正文包含 H1 标题、触发条件、工作流步骤、示例代码

### 已有 Skills（15 个）

| Skill | 用途 |
|-------|------|
| `docs-update` | 自动更新文档 |
| `github-bug-report-triage` | GitHub Bug 报告分类 |
| `github-issue-dedupe` | GitHub Issue 去重 |
| `create-pull-request` | 自动创建 PR |
| `ci-fix` | CI 失败修复 |
| `mcp-builder` | MCP Server 构建 |
| `web-performance-audit` | Web 性能审计 |
| `web-accessibility-audit` | Web 无障碍审计 |
| `webapp-testing` | Web 应用测试 |
| `seo-aeo-audit` | SEO/AEO 审计 |
| `scheduler` | 定时任务调度 |
| `slack-qa-investigate` | Slack QA 调查 |
| `terraform-style-check` | Terraform 风格检查 |
| `dbt-model-index` | DBT 模型索引 |
| `analysis-artifacts` | 分析产出管理 |

## 安装与使用

```bash
# 复制技能到项目
cp -r oz-skills/.agents/skills/<skill-name> your-project/.agents/skills/

# 或全局安装
cp -r oz-skills/.agents/skills/<skill-name> ~/.agents/skills/
```

Warp 在下一次交互时自动检测新 Skill。

## 技术架构

- 遵循 Agent Skills 开放标准（agentskills.io）
- 纯 Markdown + YAML，零依赖
- 适用于 Warp / Oz，可兼容其他支持 Agent Skills 的平台

## GitHub

https://github.com/warpdotdev/oz-skills
