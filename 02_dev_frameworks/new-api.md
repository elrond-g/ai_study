# New API

下一代 LLM 统一网关与 AI 资产管理系统，将各类大模型互转为 OpenAI/Claude/Gemini 兼容格式，适用于个人和企业的模型集中管理。

## 核心功能

- **多模型聚合** — 统一接入各类 LLM，跨格式互转（OpenAI/Claude/Gemini 兼容）
- **资产管理** — 集中管理 API Key、配额、用量统计
- **Docker 部署** — 支持 Docker Compose 一键部署，可选 SQLite 或 MySQL 后端
- **Rerank 支持** — 内置 Rerank 模型接入能力

## 快速开始

```bash
git clone https://github.com/QuantumNous/new-api.git
cd new-api
docker-compose up -d
```

默认端口 3000，支持 SQLite（默认）和 MySQL 两种存储方式。

## 技术栈

- Go 后端
- 23k+ GitHub Stars

## 链接

- GitHub: https://github.com/QuantumNous/new-api
