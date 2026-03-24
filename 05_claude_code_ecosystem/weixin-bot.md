# weixin-bot

> ⭐ 227 | Python | https://github.com/epiral/weixin-bot

## 项目简介

WeChat iLink Bot SDK，同时支持 Node.js 和 Python，零配置即可将任意 AI Agent 集成到微信。基于腾讯官方 iLink Bot API，是目前最易用的微信 Agent 接入方案之一。

## 核心功能

- **双语言 SDK**：同时提供 Node.js 和 Python 版本
- **零配置集成**：几行代码即可将 AI Agent 接入微信
- **官方 iLink API**：基于腾讯官方协议，合规稳定
- **任意 Agent 兼容**：不绑定特定 AI，可接入 Claude、GPT、本地模型等

## 快速接入示例（Python）

```python
from weixin_bot import WeixinBot

bot = WeixinBot(token="your-ilink-token")

@bot.on_message
def handle(msg):
    # 接入任意 AI Agent 处理消息
    reply = your_agent.chat(msg.text)
    return reply

bot.run()
```

## 与其他方案对比

| 方案 | 语言 | 配置复杂度 |
|------|------|------|
| weixin-bot | Python/Node.js | 低（零配置） |
| weixin-agent-sdk | TypeScript | 中（需理解 ACP） |
| cc-weixin | TypeScript | 中（demo 级） |

## 相关链接

- GitHub: https://github.com/epiral/weixin-bot
