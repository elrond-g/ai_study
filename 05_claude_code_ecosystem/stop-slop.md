# Stop Slop

去除 AI 生成文本中"机器味"的 Skill。检测并移除可预测的短语、结构模式和节奏韵律，让 AI 写作读起来更像人类。

## 核心特性

### 禁用短语库
收录需要移除的 AI 特征短语：开篇废话（"In today's..."）、强调句式（"It's worth noting..."）、商业套话、过多副词、模糊断言、元评论等。

### 结构模式过滤
识别并消除：二元对比、否定列表、戏剧性断句、修辞设问、虚假主体、旁观者叙事、被动语态。

### 句级规则
- 禁止 Wh- 句首
- 禁用破折号滥用
- 无断奏式碎片化
- 必须使用主动语态

### 5 维评分体系
每段文字按以下维度 1-10 打分：
- 直接性 | 节奏 | 信任感 | 真实感 | 密度
- 低于 35/50 需重写

## 技术架构

- **格式**：SKILL.md + references/
- **集成**：Claude Code Skill、Claude Projects、自定义指令、API 系统提示

## 安装与使用

```bash
# Claude Code: 添加为 Skill
# 或上传至 Claude Projects
# 或复制核心规则到 API system prompt
```

## GitHub

https://github.com/hardikpandya/stop-slop
