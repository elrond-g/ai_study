# claude-statusline

简洁实用的双行 Claude Code 状态栏，显示关键信息，隐藏无关内容。~30ms 渲染。

## 显示内容

### 第一行 — AI 状态与用量

```
Model │ Context Bar 28% │ $0.42 │ 5h 45% ↺ 4h27m │ 7d 12% ↺ 5d2h
```

模型名称、上下文进度条（16 段）、会话费用、5 小时/7 天 API 配额及重置倒计时。90%+ 上下文时显示红色警告。

### 第二行 — 工作区

```
my-project │ main +2 ~1 ?3 │ .venv (3.12) │ NORMAL
```

目录名、Git 分支 + 文件状态、Python venv（检测到时显示）、Vim 模式（启用时显示）。

## 设计理念

- **实用优先**：不影响下一步操作的信息不上状态栏
- **默认安静**：可选段（venv、vim mode）仅在相关时出现
- **一目了然**：两行，颜色编码（绿 0-49%、黄 50-79%、红 80%+）
- **极速渲染**：单次 jq + 单次 git status + 后台缓存 API 调用，~30ms

## 安装

```bash
curl -fsSL https://raw.githubusercontent.com/tzengyuxio/claude-statusline/main/install.sh | bash
```

需要 bash 4.0+、jq、git 和 Nerd Font。

## 链接

- GitHub: https://github.com/tzengyuxio/claude-statusline
