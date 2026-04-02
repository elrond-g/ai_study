# hucre

> GitHub | https://github.com/productdevbook/hucre

## 项目简介

hucre 是一个零依赖的纯 TypeScript 电子表格引擎，支持读写 XLSX、CSV、ODS 格式，可运行在任何 JavaScript 环境中（Node.js、浏览器、Deno、Bun 等）。

## 核心特点

- **零依赖**：无任何第三方依赖
- **纯 TypeScript**：完整的类型安全
- **多格式支持**：XLSX 读写、CSV 解析/生成、ODS 解析
- **Tree Shaking 友好**：按需导入，XLSX 仅 ~14KB gzipped，CSV 仅 ~2KB gzipped
- **Schema 验证**：内置数据验证
- **流式处理**：支持流式读写大文件
- **Round-trip 保留**：读取后再写入保持原始格式

## 快速示例

```ts
import { readXlsx, writeXlsx } from "hucre";

// 读取 XLSX
const workbook = await readXlsx(buffer);

// 按需导入
import { readXlsx, writeXlsx } from "hucre/xlsx"; // ~14 KB
import { parseCsv, writeCsv } from "hucre/csv";   // ~2 KB
```

## 技术规格

- **语言**：TypeScript
- **Stars**：686
- **许可证**：开源

## 相关链接

- GitHub: https://github.com/productdevbook/hucre
- NPM: https://npmjs.com/package/hucre
