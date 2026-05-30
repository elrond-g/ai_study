# Claude Code Plugins Official

Anthropic 官方维护的高质量 Claude Code 插件目录。包含内部开发插件（/plugins）和第三方社区插件（/external_plugins），提供标准化的插件安装和发现机制。

## 核心特性

### 官方维护
由 Anthropic 团队维护，确保插件质量和安全审查标准。

### 标准化结构
每个插件遵循统一目录结构：plugin.json 元数据、可选的 MCP 配置、commands、agents、skills 等。

### Skill-bundle 支持
支持无 plugin.json 的纯 Skills 仓库作为插件发布，通过 marketplace 声明显式 skills 数组。

### 市场发现
Claude Code 中通过 /plugin discover 浏览和安装插件。

## 技术架构

- **维护方**：Anthropic
- **结构**：/plugins（内部）+ /external_plugins（社区）
- **安装**：/plugin install {name}@claude-plugins-official

## 安装与使用

```bash
# Claude Code 中使用
/plugin install {plugin-name}@claude-plugins-official
/plugin discover
```

## GitHub

https://github.com/anthropics/claude-plugins-official
