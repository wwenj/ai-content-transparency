<div align="center">

# AI Content Transparency

<p>
  <a href="./README.md">中文</a>
  ·
  <a href="./README.en.md">English</a>
</p>

<p>🪧 面向 AI 参与内容创作的透明声明倡议与轻量生成工具</p>

<p>
  <a href="https://wwenj.github.io/ai-content-transparency/generator/index.html">快速使用生成器</a>
</p>

</div>

## 项目简介

`ai-content-transparency` 是一个用于内容创作场景的 AI 透明声明项目，目标是以简洁、明确、可落地的方式说明 AI 在内容生产中的参与比例与职责分工。

项目同时提供一个可直接在线访问的声明卡片生成器，用于快速生成适合文章开头展示的说明图片。

## 为什么需要这个项目

随着 AI 写作、改写、润色、整理能力快速普及，越来越多内容已经不再是纯人工完成，但大多数作品并没有明确说明 AI 是否参与、参与了多少、具体承担了什么角色。这会导致：

- 读者无法准确判断内容的生产方式
- 创作者之间缺少统一、清晰的声明口径
- “完全人工”与“高度 AI 参与”的边界被模糊化

本项目的立场很明确：`不禁止 AI，但强调透明优先`。

## 核心原则

### 1. 透明优先

当 AI 对最终内容形成实质性参与时，应以清晰、可见、易理解的方式进行说明。

### 2. 不反对使用 AI

本项目不将 AI 视为应被排斥的工具。我们反对的是隐瞒使用、模糊表述、或故意误导受众。

### 3. 人类责任保留

无论是否使用 AI，最终发布者仍应对事实准确性、价值判断、内容表达和发布结果负责。

### 4. 声明应尽量具体

相较于“部分 AI 辅助”这类模糊说法，更推荐明确说明：

- AI 占比 `ai_ratio`
- 人类占比 `human_ratio`
- AI 分工 `ai_roles`
- 人类分工 `human_roles`

### 5. 自愿采用

本项目是开源倡议，不是法律规则、不是平台强制要求，也不是认证体系。其价值来自创作者的自律与社区共识。

## 声明规范

建议采用以下四个核心字段：

| 字段 | 含义 | 说明 |
| --- | --- | --- |
| `ai_ratio` | AI 占比 | `0-100` 的整数 |
| `human_ratio` | 人类占比 | `0-100` 的整数，且与 `ai_ratio` 之和为 `100` |
| `ai_roles` | AI 分工 | AI 实际承担的任务列表 |
| `human_roles` | 人类分工 | 人类实际承担的任务列表 |

### 示例

```json
{
  "version": "1.0",
  "ai_ratio": 35,
  "human_ratio": 65,
  "ai_roles": [
    "提纲起草",
    "语言润色",
    "标题建议"
  ],
  "human_roles": [
    "选题确定",
    "论证设计",
    "事实复核",
    "最终审核"
  ],
  "note": "作者自愿进行的透明声明。"
}
```

### 展示要求

1. 声明建议放在文章、页面或帖文开头
2. 不应藏在脚注、折叠区域或不易发现的位置
3. 不应使用会误导读者的措辞
4. 若使用图片卡片，建议同时保留文本版本

## 快速使用

### 在线生成器

- 直接访问：[https://wwenj.github.io/ai-content-transparency/generator/index.html](https://wwenj.github.io/ai-content-transparency/generator/index.html)

### 使用步骤

1. 输入 AI 占比与人类占比
2. 生成卡片并导出图片
3. 将声明卡片或文本声明放在内容开头

## 示例预览

![Example 1](./examples/example1.png)

![Example 2](./examples/example2.png)

## 适用场景

- 博客文章
- 知识付费内容
- 技术文档
- 资讯整理
- 研究笔记
- 自媒体长文

## 开源说明

- License: [MIT](./LICENSE)
- Generator: [generator/index.html](./generator/index.html)

