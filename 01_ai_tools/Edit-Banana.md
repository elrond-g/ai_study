# Edit-Banana

> ⭐ 4,464 | Python | https://github.com/BIT-DataLab/Edit-Banana | https://editbanana.anxin6.cn/

## 项目简介

Edit-Banana 是北京理工大学数据实验室开源的框架，专注于将 AI 统计生成的图表和可视化格式转换为可编辑的标准格式。解决了 AI 生成图片"只能看不能改"的痛点，让用户可以进一步编辑 AI 产出的数据可视化成果。

## 核心功能

- **格式转换**：将 AI 生成的静态图像转换为可编辑的矢量/数据格式
- **NanoBanana 引擎**：轻量化的图表解析内核
- **多格式支持**：覆盖常见统计图表类型（折线图、柱状图、饼图等）
- **LLM 集成**：利用多模态大模型理解图表内容并重建数据

## 技术特点

- Python 实现，依赖 PyTorch 和 OpenCV
- 结合 OCR 和视觉理解技术提取图表数据
- 支持导出为 Excel、CSV、SVG 等可编辑格式

## 使用场景

- 从论文截图或报告图片中提取可编辑的数据
- 对 AI 生成的数据可视化进行二次编辑和定制
- 数据分析工作流中的图表格式转换环节

## 相关链接

- GitHub: https://github.com/BIT-DataLab/Edit-Banana
- 演示: https://editbanana.anxin6.cn/
