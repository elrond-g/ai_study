# kicad-happy

> https://github.com/aklofas/kicad-happy

## 项目简介

kicad-happy 是一个让 AI Agent 在终端中完成 PCB 硬件设计的 Claude Code Skill，通过 KiCad 命令行接口让 Claude 直接操控 PCB 设计流程——绘制原理图、布局 PCB、生成 Gerber 文件，无需手动操作 KiCad GUI。

## 核心功能

- **原理图生成**：用自然语言描述电路，AI 生成 KiCad 原理图
- **PCB 布局**：自动摆放元器件、完成布线
- **设计规则检查**：自动运行 DRC，修复违规
- **生产文件导出**：Gerber、钻孔文件一键生成

## 技术特点

- 与 KiCad CLI 深度集成
- 内置硬件设计规范和常见电路模式知识
- 支持从需求描述到可生产 PCB 的完整流程

## 使用场景

- 软件工程师快速验证简单硬件原型
- 硬件工程师加速 PCB 设计迭代
- 探索 AI 驱动的硬件设计新范式

## 相关链接

- GitHub: https://github.com/aklofas/kicad-happy
