# Dograh AI

开源语音 AI 平台，可自托管替代 Vapi 和 Retell。提供拖拽式工作流构建器，支持 BYOK（自带 LLM/STT/TTS），2 分钟内即可搭建可用的语音机器人。由 YC 校友和成功退出创始人维护。

## 核心特性

### 100% 开源可自托管
BSD 2-Clause 许可，一条 Docker 命令即可部署，无厂商锁定。

### 可视化工作流构建
拖拽式界面设计对话流程，无需编码即可构建复杂的语音交互逻辑。

### 灵活的模型集成
支持接入任意 LLM、STT、TTS 提供商，也可以使用 Dograh 内置的模型栈。

### MCP 原生支持
原生支持 Model Context Protocol，可与各种 MCP 服务集成。

### 电话支持
除 WebRTC 外还支持传统电话线路接入。

## 技术架构

- **许可**：BSD 2-Clause
- **部署**：Docker 一键部署
- **框架**：灵活可插拔的提供商架构
- **对比 Vapi/Retell**：完全开源、可自托管、源码级定制

## 安装与使用

```bash
# Docker 一键部署
docker run -p 3000:3000 dograhhq/dograh
```

## GitHub

https://github.com/dograh-hq/dograh
