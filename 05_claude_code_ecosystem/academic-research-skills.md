# Academic Research Skills (ARS)

> ⭐ Claude Code Skill 套件 | v3.9.4.2 | https://github.com/Imbad0202/academic-research-skills

## 项目简介

面向 Claude Code 的完整学术研究 Skill 套件，覆盖从研究到发表的全流程管线。核心理念是"AI 是副驾驶，不是飞行员"——ARS 处理查找文献、格式化引用、验证数据、检查逻辑一致性等繁重工作，让研究者专注于定义问题、选择方法和解读数据。

## 核心特性

### Deep Research（7 种模式）
13 个 Agent 组成的研究团队：完整模式、快速简报、PRISMA 系统综述、苏格拉底引导模式、事实核查、文献综述、审阅模式。内置意图检测层和对话健康监控。

### Academic Paper（10 种模式）
12 个 Agent 的论文写作管线：风格校准（学习你的写作风格）、写作质量检查（检测 AI 常见表达模式）、LaTeX 加固、可视化、修订教练、引用格式转换。输出 MD + DOCX + LaTeX PDF。

### Academic Paper Reviewer（6 种模式）
7 个 Agent 的多视角同行评审：EIC + 3 位动态审稿人 + Devil's Advocate，0-100 质量评分标准，让步阈值协议防止审查让步过快。

### Academic Pipeline（10 阶段编排器）
自适应检查点 + 声明验证 + Material Passport + 交叉模型完整性验证 + 协作深度评估。

### 关键创新
- **Devil's Advocate 让步阈值**：DA 必须先评分反驳再回应，仅 ≥4 分允许让步，防止"被怼就怂"
- **反泄漏协议**：优先使用会话材料而非模型参数记忆，防止幻觉引用
- **引用审计**：v3.8 引入声明级引用验证（`ARS_CLAIM_AUDIT=1`），发现实际案例中 31% 引用通过 3 轮完整性检查仍有问题
- **7 种 AI 研究失败模式检查**：阻止实现 Bug/幻觉结果/捷径依赖/Bug-当-洞察/方法论伪造/框架锁定

## 安装

```bash
# Claude Code 插件安装（推荐，30 秒）
/plugin marketplace add Imbad0202/academic-research-skills
/plugin install academic-research-skills
```

## 成本估算

完整管线处理一篇 15K 单词论文约 $4–6（按 Claude 模型 API 价格估算）。

## GitHub

https://github.com/Imbad0202/academic-research-skills
