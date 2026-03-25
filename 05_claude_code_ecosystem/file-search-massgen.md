# File Search / massgen

> ⭐ N/A | Markdown (Skill) | https://github.com/massgen/massgen

## 项目简介

基于 Ripgrep 和 ast-grep 的深度代码搜索 Skill，为 Claude Code 提供结构化语法感知的代码检索能力。

## 核心功能

- **Ripgrep 全文搜索**：毫秒级全仓库文本搜索，支持正则表达式和文件类型过滤
- **ast-grep 语法搜索**：基于 AST 抽象语法树匹配代码模式，精准定位函数、类和变量
- **组合搜索策略**：先用文本搜索缩小范围，再用语法搜索精确匹配，提升搜索效率

## 技术特点

- 结合字符串搜索与 AST 结构化搜索，兼顾速度和精度
- 支持多语言语法解析：JavaScript、TypeScript、Python、Rust 等
- 搜索结果自动格式化，便于 Claude 理解和引用代码片段

## 使用场景

- 在大型单体仓库中快速定位特定函数或 API 调用
- 重构前批量查找某一代码模式的所有实例
- 代码审查中搜索潜在的安全问题或反模式

## 相关链接

- GitHub: https://github.com/massgen/massgen
