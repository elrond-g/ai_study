# OpenBB

> ⭐ 59,856+ | Python (FastAPI) | https://github.com/OpenBB-finance/OpenBB | https://openbb.co | MIT

## 项目简介

OpenBB 是面向分析师、量化交易员和 AI Agent 的开源金融数据平台，定位为"AI 驱动的金融工作空间"。核心理念"一次连接，随处消费"——整合近 100 个数据源，通过 Python SDK / CLI / REST API / MCP Server / Excel 五种接口统一访问，覆盖股票、期权、加密货币、外汇、宏观经济、固定收益和替代数据集。

## 五种访问接口

| 接口 | 面向用户 |
|------|----------|
| Python SDK | 量化开发者，类型提示 + 完整文档 |
| CLI | 命令行用户 |
| FastAPI REST | 第三方系统集成 |
| OpenBB Workspace | 企业分析师，数据可视化 + AI 分析 |
| Excel 集成 | 传统分析师，熟悉的电子表格环境 |
| MCP Server | AI Agent 标准化接口 |

## 数据覆盖

**近 100 个数据提供商**，350+ 金融数据集：
- **市场数据**：Alpha Vantage、Benzinga 等
- **经济数据**：FRED（816,000+ 经济时间序列）、Trading Economics（196 国 2000 万+ 指标）
- **政府数据**：EIA（能源）、美国国会、IMF、BLS
- **资产类别**：股票/ETF、期权、加密货币、外汇、宏观、固收、替代数据

## 技术架构

```
openbb-core（核心逻辑 + REST API）
  ├── Routers 层（openbb-equity / openbb-economy 等）
  ├── Providers 层（数据提供商集成）
  ├── QueryExecutor（transform_query → extract_data → transform_data）
  └── OBBject（标准化响应：.to_dataframe() / .to_dict()）
```

- Python + FastAPI + Pydantic
- 模块化插件系统，PackageBuilder 动态生成 SDK 模块
- 自定义数据源通过 Python 扩展集成

## AI Agent 集成

- **MCP Server**：为 AI Agent 提供标准化金融数据接口
- **Pydantic AI 集成**：官方示例 + agents-for-openbb 参考实现
- **Agent 能力**：
  - 响应式查询：回答市场状况、公司表现问题
  - 主动式监控：监测仪表板异常、趋势和机会
  - 动态组合多数据源的高级分析
  - 精细化数据访问控制

## 项目规模

59,856+ Stars、5,835 Forks、247+ 贡献者、4,793 个合并 PR

## 为什么值得关注

1. **开源金融数据的事实标准**：6 万 Stars，近 100 个数据源统一访问
2. **AI-Ready 设计**：MCP + REST + Pydantic AI，从架构层面原生支持 Agent
3. **全角色覆盖**：分析师用 Excel/Workspace，量化用 SDK，Agent 用 MCP/API
4. **零数据费**：平台本身免费，只需支付数据提供商 API 费用
5. **标准化处理**：自动屏蔽不同数据源格式差异，统一输出

## 使用场景

- 金融数据研究和分析
- 量化交易系统开发
- AI 驱动的投资研究工作流
- 企业级财务数据平台搭建
- AI Agent 金融能力扩展（通过 MCP）

## 相关链接

- GitHub: https://github.com/OpenBB-finance/OpenBB
- 官网: https://openbb.co
- 文档: https://docs.openbb.co
- Agent 集成: https://docs.openbb.co/workspace/developers/agents-integration
