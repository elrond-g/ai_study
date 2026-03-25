# OpenDeepWiki

DeepWiki 的开源版本，基于 .NET 9 + Semantic Kernel 构建的 AI 驱动代码知识库平台。输入代码仓库 URL，自动生成结构化、可搜索的多语言文档。

## 核心特性

- **自动代码分析**：解析代码结构，理解仓库核心概念，生成代码文档和 README
- **五阶段 AI 流水线**：准备（克隆过滤）→ 分析（思维导图/目录/概览）→ 内容生成（GATHER/THINK/WRITE 三阶段）→ 翻译（多语言）→ 输出
- **知识图谱生成**：自动构建代码仓库的知识图谱和思维导图
- **多平台支持**：接受 GitHub、GitLab、Gitee 等 Git 平台的仓库 URL
- **MCP 集成**：可作为 MCP Server 供其他 AI 模型调用，辅助分析开源项目
- **多语言文档**：从源语言自动翻译生成中文、日文、韩文等版本

## 技术栈

- 后端：C# / .NET 9 / Semantic Kernel
- 前端：TypeScript
- 模块化设计，易于扩展和定制

## 链接

- GitHub: https://github.com/AIDotNet/OpenDeepWiki
