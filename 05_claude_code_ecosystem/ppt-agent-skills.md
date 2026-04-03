# PPT Agent Skills

> GitHub | https://github.com/sunbigfly/ppt-agent-skills

## 项目简介

基于软件工程理念的演示文稿全自动生成框架，以 Agent Skill 形式运行。状态机驱动多 Agent 协作，将一句话需求输出为专业级 PPTX 文件，从根源解决传统大模型生成的幻觉、重叠与布局混乱问题。

## 安装

```
npx skills add sunbigfly/ppt-agent-skills
```

## 核心亮点

- **Subagent 阶段隔离**：Research / Outline / Style / Planning 四大阶段各自运行独立子代理，Context 不互染
- **像素级 Visual QA 闭环**：每页 HTML 构建后自动截图，大模型视觉审计，检测到布局溢出后以 DOM + CSS 结构重写消除冲突
- **无状态断点恢复**：不依赖进度状态文件，中断后扫描磁盘已有产物自动推断恢复点
- **数据层与渲染层隔离**：先生成 JSON 合同并通过 `planning_validator.py` 校验，再驱动 HTML 渲染
- **双引擎 PPTX 导出**：PNG 光栅流 100% 视觉还原 + SVG 矢量流保留字体可编辑

## 工作流

```
P0 采访 → P1 分支确认
P2A 联网检索 / P2B 本地资料压缩
P3 叙事大纲 → P3.5 全局风格锁定
P4 逐页并行生产（Planning → HTML → Visual QA）
P5 Preview + 双 PPTX 导出
```

## 规模参数

- 6 个阶段流水线
- 8 套主题风格
- 10 种版式类型
- 13 种图表模板
- 8 类组件库
- 14 个脚本工具

## 相关链接

- GitHub: https://github.com/sunbigfly/ppt-agent-skills
