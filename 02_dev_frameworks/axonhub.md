# axonhub

> ⭐ 2,693 | Go | https://github.com/looplj/axonhub

## 项目简介

开源 AI Gateway，允许使用任意 SDK（OpenAI、Anthropic 等）调用 100+ LLMs，并在网关层统一提供故障转移、负载均衡、成本控制和全链路追踪能力。

## 核心功能

- **100+ LLM 接入**：一套接口调用 OpenAI、Anthropic、Google、Mistral 等所有主流模型
- **故障转移**：主模型不可用时自动切换到备用模型
- **负载均衡**：在多个 API Key 或模型端点间分配请求
- **成本控制**：按项目/用户设置 Token 消耗上限和预算告警
- **全链路追踪**：记录每次请求的延迟、Token 用量、费用，支持可视化查询

## 技术特点

- Go 实现，性能高、部署简单，单二进制文件
- 兼容 OpenAI API 格式，现有代码无需修改即可接入
- 支持 Docker 部署，适合团队内部共享网关

## 使用场景

- 团队共享 AI API Key，统一管控成本和用量
- 多模型 A/B 测试，透明切换不影响业务代码
- 生产环境需要高可用的 LLM 调用层

## 相关链接

- GitHub: https://github.com/looplj/axonhub
