# qclaw-wechat-client

> https://github.com/photon-hq/qclaw-wechat-client

## 项目简介

qclaw-wechat-client 是从 QClaw（微信版 Claude/Claw 客户端）逆向工程得到的微信接口实现，提供可编程的微信通信能力，可用于将 Claude/Claw Agent 与微信生态打通。

## 核心功能

- **微信消息收发**：通过代码发送和接收微信消息
- **群组管理**：支持群消息监听和发送
- **AI 集成**：将 Claude/Claw 的 AI 能力接入微信通讯场景
- **自动化响应**：基于关键词或 AI 判断自动响应微信消息

## 技术来源

项目基于对 QClaw 客户端的逆向工程，QClaw 是一款将 Claude AI 集成进微信的工具。逆向后开放了其底层微信接口，可供开发者二次开发。

## 使用场景

- 在微信群或私聊中部署 Claude AI 助手
- 构建微信 + AI 的自动化工作流
- 研究微信通信协议和 AI 集成方案

## 注意事项

微信不开放官方 API，此类工具存在账号被封禁的风险。建议在测试账号上使用，不要在主要账号上运行。

## 相关链接

- GitHub: https://github.com/photon-hq/qclaw-wechat-client
