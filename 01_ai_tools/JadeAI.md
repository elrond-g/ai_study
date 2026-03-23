# JadeAI

> ⭐ 929 | TypeScript | https://github.com/twwch/JadeAI | https://jadeai.cturing.cn/en

## 项目简介

JadeAI 是一款 AI 驱动的智能简历生成器，提供 50+ 专业模板，支持 PDF/图片解析、AI 内容优化、岗位匹配分析和多格式导出。完全开源免费，支持一键 Docker 部署。

## 核心功能

- **50+ 专业模板**：覆盖技术、设计、金融、学术等各类职业场景
- **PDF/图片解析**：上传现有简历自动提取内容，无需重新录入
- **AI 内容优化**：基于 JD（职位描述）智能调整简历措辞和侧重点
- **JD 匹配分析**：量化简历与目标岗位的匹配程度
- **多格式导出**：支持 PDF、Word、图片等格式

## 技术特点

- TypeScript + Next.js 全栈，前后端一体
- Docker 一键部署，5 分钟上线私有实例
- 支持接入 OpenAI、Claude 等多个 LLM 后端

## 使用场景

- 求职者快速生成针对特定岗位的定制简历
- HR 工具集成，批量生成标准化人才档案
- 自部署私有简历平台，保护个人数据隐私

## 快速开始

```bash
docker run -d -p 3000:3000 twwch/jadeai
```

## 相关链接

- GitHub: https://github.com/twwch/JadeAI
- 演示: https://jadeai.cturing.cn/en
