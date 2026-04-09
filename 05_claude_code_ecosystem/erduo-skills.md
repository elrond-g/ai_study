# erduo-skills（耳朵技能库）

> ⭐ 800+ | JavaScript/Python | https://github.com/rookie-ricardo/erduo-skills

## 项目简介

erduo-skills 是一个 AI Agent 结构化技能库，收录了一系列可被 Agent 直接调用的独立、可组合工作流单元。覆盖信息获取、内容处理、翻译、图像工具等场景，通过 `npx skills add` 一键安装供 Claude Code 等 Agent 调用。

## 技能一览

| 技能 | 简介 | 调用方式 |
|------|------|----------|
| 每日日报 | 多源抓取 + 智能筛选，自动生成技术日报 | Agent 调用 |
| AK RSS Digest | 固定 RSS 源精选摘要，10 分制打分过滤 | Agent / CLI |
| 转录精修师 | 语音转录文本 → 可读文章，保留原汁原味 | Agent 调用 |
| 翻译精修师 | 分析→初译→审校→终稿四步精翻工作流 | Agent 调用 |
| Web To Markdown | URL 路由抓取 + Readability 清洗，输出干净 Markdown | Agent / CLI |
| Gemini 水印移除 | 逆向 Alpha 混合去除 Gemini 图片水印 | CLI |

## 技术特点

- **Master-Worker 架构**（日报）：主 Agent 调度决策，子 Agent 并行抓取，支持无头浏览器处理 JS 渲染页面
- **10 分制打分 + 去重**：URL + 内容哈希双重校验，早停机制（20+ 高质量条目即停止）
- **四步翻译工作流**：术语提取→修辞映射→读者理解障碍分析→翻译，支持 ZH↔EN、ZH↔JA，内置 9 种风格预设
- **转录精修**：自动识别单人/多人模式，降噪（口水词、无意义附和）、同音字纠错、语义分段，长文本自动分 chunk 并行处理
- **URL 智能路由**（Web To Markdown）：通用网页走 `r.jina.ai`，YouTube 走 `defuddle.md`，微信/知乎/飞书走 Chrome 指纹 HTTP 抓取
- **逆向 Alpha 混合**（水印移除）：`original = (watermarked - alpha × logo) / (1 - alpha)`，纯 Python + Pillow

## 安装方式

```bash
# 全部安装
npx skills add rookie-ricardo/erduo-skills

# 单独安装某个技能
npx skills add rookie-ricardo/erduo-skills --skill daily-news-report
npx skills add rookie-ricardo/erduo-skills --skill translate-polisher
```

## 为什么值得关注

六个技能覆盖了信息工作者的高频场景——新闻聚合、RSS 筛选、语音转文字、翻译、网页提取、图片处理。每个技能独立可组合，Master-Worker 并行架构和智能路由策略体现了成熟的 Agent Skill 设计思路。

## 相关链接

- GitHub: https://github.com/rookie-ricardo/erduo-skills
