# writing-style-skill

可复用的写作风格 Skill 模板，内置自动学习机制。AI 写初稿，你修改到满意，自动从 diff 中提取写作规则，SKILL.md 越用越准。

## 原理

```
AI 用 SKILL.md 写初稿 → 你改到满意 → diff 两版 → 提取规则 → 更新 SKILL.md → 下次更准
```

只需两个数据点：original（AI 第一版）和 final（你最终版），中间改了多少轮不管。

## 核心特性

- **自动学习**：从你的修改中自动提取写作规则
- **置信度分级**：规则按 P0/P1/P2 分级，P0 自动应用
- **自动备份**：每次更新前自动备份，支持一键回滚
- **零依赖观察**：`observe.py` 纯 Python，无第三方依赖
- **多 LLM 支持**：自动检测 claude / llm CLI / 自定义命令
- **兼容平台**：Claude Code + OpenClaw (ClawHub)

## 使用流程

1. 修改 SKILL.md 模板为你的风格（或留空让自动学习填充）
2. 让 AI 用此 Skill 写内容
3. 修改到满意
4. `python3 scripts/observe.py record-original draft.md` + `record-final final.md`
5. `python3 scripts/improve.py auto --skill .` 提取规则

## 链接

- GitHub: https://github.com/jzocb/writing-style-skill
