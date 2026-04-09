# Capstan

> ⭐ 12 | TypeScript | https://github.com/barry3406/capstan

## 项目简介

Capstan 是一个以 Bun 为主要运行时的全栈 TypeScript 框架，核心理念是"Agent-operable by default"——让应用天然可被 AI Agent 操作。通过一次 `defineAPI()` 定义，同时生成 HTTP、MCP、Google A2A、OpenAPI 四种协议端点，让人类与 AI Agent 共享同一应用契约。

## 核心功能

- **`defineAPI()` 统一契约**：一次定义自动生成 REST API（Hono）、MCP Tool（stdio/Streamable HTTP）、A2A Skill（SSE）、OpenAPI 3.1 规范
- **Policy & Approval 原语**：`definePolicy()` 支持 allow/deny/approve/redact 四种效果，Agent 写操作可触发 human-in-the-loop 审批
- **AI TDD 验证循环**：8 步验证级联，`capstan verify --json` 输出结构化修复清单供 AI 编码助手自动修复
- **Durable Agent Runtime**：`createHarness()` 提供持久化运行、检查点、任务记录、浏览器/文件系统沙盒
- **MCP Client**：handler 中通过 `connectMCP()` 消费外部 MCP 服务器
- **向量字段 & RAG**：`field.vector()`、`defineEmbedding`、混合搜索内置于 ORM

## 全栈能力

- 文件式路由：`.page.tsx`（React SSR）、`.api.ts`、`_layout.tsx`、`_middleware.ts`
- Zod Schema 跨协议类型安全
- Drizzle ORM 声明式数据模型（SQLite/PostgreSQL/MySQL），自动生成 CRUD 路由
- React SSR + 选择性 hydration、SPA 路由、View Transitions
- 内置 LLM Provider（OpenAI + Anthropic）、LangChain 集成
- OAuth（Google/GitHub）、DPoP、SPIFFE/mTLS、token-aware 限流
- OpenTelemetry 跨协议追踪
- 部署适配器：Cloudflare Workers、Vercel、Fly.io、Docker

## 技术特点

- Bun 原生运行时（也支持 Node.js）
- TypeScript 全栈
- 12 个 workspace 包（CLI、dev server、ops 运行时、cron 调度器等）
- v1.0.0-beta.8，MIT 许可

## 使用场景

- 构建天然可被 AI Agent 操控的全栈应用
- 需要同时暴露 HTTP + MCP + A2A 多协议的服务
- Agent-first 的 SaaS 应用开发

## 相关链接

- GitHub: https://github.com/barry3406/capstan
