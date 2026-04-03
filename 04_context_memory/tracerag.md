# TraceRAG

> GitHub | https://github.com/youngjoey-ai/tracerag

## 项目简介

TraceRAG 是一个强调工程化、可观测、可测试、可扩展的生产级 RAG 项目。目标不是只把答案"生成出来"，而是将文档导入、切块、向量化、检索、带来源回答、评估与 Tracing 拆成可独立验证的阶段，逐步演进成可维护、可解释、可复盘的系统。

## 核心闭环

```
文档导入 → 切块 → Embedding → 向量检索 → 带 sources 的回答 → Eval 驱动迭代
```

## 已实现功能

- `POST /import`：文档导入 + 切块
- `POST /embed/{document_id}`：向量生成写入 pgvector
- `GET /retrieve`：向量检索、Top-K、按 source 过滤
- `GET /ask`：LangGraph 编排 retrieve → generate，返回 answer + sources + duration_ms，Redis 缓存
- `GET /retrieve_hybrid`：向量检索 + BM25 + RRF 融合 + 关键词 rerank
- Alembic 迁移 + HNSW 索引
- Langfuse 全链路 tracing + prompt 版本管理
- LLM-as-a-judge 评估：faithfulness 0.97、answer_relevance 1.00
- API Key 认证

## 技术栈

| 模块 | 选择 |
|------|------|
| API 框架 | FastAPI |
| 数据库 | PostgreSQL + pgvector |
| ORM/迁移 | SQLAlchemy + Alembic |
| 切块 | LangChain RecursiveCharacterTextSplitter |
| Embedding/LLM | DashScope（text-embedding-v3 + qwen-plus） |
| 工作流编排 | LangGraph |
| 检索 | pgvector cosine + PostgreSQL FTS + Hybrid |
| 缓存 | Redis（相同问题 <5ms 响应） |
| 可观测性 | Langfuse |
| 评估 | LLM-as-a-judge |

## 设计原则

- 先独立验证 retrieval，再接入 LLM，降低排错成本
- 所有优化有数据支撑，不靠主观感觉
- 贴近 2026 工程实践：pgvector、Alembic、Eval、Hybrid Search、Tracing

## 相关链接

- GitHub: https://github.com/youngjoey-ai/tracerag
