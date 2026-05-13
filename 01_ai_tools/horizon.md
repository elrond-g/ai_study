# Horizon

AI 驱动的新闻雷达，从 Hacker News / Reddit / Telegram / RSS / GitHub / Twitter/X 等多源聚合信息，经 AI 评分去重过滤后生成中英双语文档，支持网页/邮件/飞书/钉钉/Slack/Discord 多渠道分发。8K Stars。

## 核心特性

### 多源聚合
- Hacker News / Reddit / Telegram / RSS / GitHub Releases & 用户动态 / Twitter/X
- 自定义源配置，支持社区源共享

### AI 智能处理
- **评分筛选**：Claude / GPT / Gemini / DeepSeek / Doubao / MiniMax 等多模型 0-10 打分
- **去重合并**：跨平台相同新闻自动合并
- **背景增强**：Web 搜索补充不熟悉的概念/公司/项目/技术术语
- **评论摘要**：收集并总结 Hacker News / Reddit 等社区讨论
- **社区源中心**：人类策划的隐藏信息源

### 多渠道分发
- GitHub Pages 日更站点
- 自托管 SMTP/IMAP 邮件通讯（自动订阅/退订）
- 飞书 / 钉钉 / Slack / Discord / 自定义 Webhook
- MCP Server 集成

### 工作流程
```
配置源 → 拉取 → 去重 → AI 评分过滤 → 背景增强 → 摘要 → 多语种输出 → 多渠道分发
```

## 安装与使用

```bash
# 克隆仓库
git clone https://github.com/Thysrael/Horizon.git

# 配置源和输出
编辑 config.json

# Docker 运行（推荐）
docker compose up -d

# 或本地 Python 运行
uv run horizon

# Setup Wizard 生成个性化配置
uv run horizon --wizard

# 访问日更站点
# https://<your-username>.github.io/Horizon/
```

## 技术架构

- **语言**：Python（uv 包管理，pyproject.toml）
- **部署**：Docker + GitHub Actions（自动日更）
- **模型**：支持 OpenAI 兼容 API，内置多模型适配
- **输出**：Markdown → GitHub Pages 静态站点
- **通知**：飞书 Webhook / 钉钉 / Slack / Discord / SMTP 邮件 / MCP

## 与其他新闻聚合工具对比

| 特性 | Horizon | GPT Researcher | 传统 RSS |
|------|---------|---------------|---------|
| AI 评分筛选 | ✅ | ✅ | ❌ |
| 多源去重 | ✅ | ❌ | ❌ |
| 社区评论摘要 | ✅ | ❌ | ❌ |
| 中英双语 | ✅ | ❌ | ❌ |
| 多渠道分发 | ✅ | ❌ | ❌ |
| 自托管 | ✅ | ✅ | ✅ |

## GitHub

https://github.com/Thysrael/Horizon
