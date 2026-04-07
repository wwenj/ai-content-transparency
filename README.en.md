<div align="center">

# AI Content Transparency

<p>
  <a href="./README.md">中文</a>
  ·
  <a href="./README.en.md">English</a>
</p>

<p>🪧 A lightweight transparency initiative and generator for AI-assisted content creation</p>

<p>
  <a href="https://wwenj.github.io/ai-content-transparency/generator/index.html">Open Generator</a>
</p>

</div>

## Overview

`ai-content-transparency` is an open project for disclosing AI participation in content creation in a simple, explicit, and practical way. It helps creators state how much AI was involved and what roles were handled by AI versus humans.

The project also provides a browser-based card generator for creating declaration images that can be placed at the beginning of an article or page.

## Why This Project

AI is now widely used for drafting, polishing, rewriting, summarizing, and structuring content. However, most published work still does not clearly state whether AI participated, how much it contributed, or which tasks it handled. This leads to several problems:

- readers cannot accurately judge how the content was produced
- creators lack a simple and consistent disclosure format
- the boundary between human-led work and heavily AI-assisted work becomes unclear

The position of this project is straightforward: `AI is allowed, but transparency comes first`.

## Core Principles

### 1. Transparency First

If AI materially contributes to the final content, that participation should be disclosed in a visible and understandable way.

### 2. AI Is Not Prohibited

This project does not oppose AI usage. It opposes hidden usage, vague statements, and misleading presentation.

### 3. Human Responsibility Remains

The final publisher remains responsible for factual accuracy, judgment, framing, and the consequences of publication, regardless of which tools were used.

### 4. Disclosure Should Be Specific

Instead of vague wording such as “partially AI-assisted,” this project recommends clearly stating:

- AI ratio `ai_ratio`
- Human ratio `human_ratio`
- AI roles `ai_roles`
- Human roles `human_roles`

### 5. Voluntary Adoption

This is an open initiative, not a law, not a platform policy, and not a certification system. Its value depends on creator self-discipline and community adoption.

## Disclosure Specification

The recommended minimum structure contains four core fields:

| Field | Meaning | Notes |
| --- | --- | --- |
| `ai_ratio` | AI contribution ratio | Integer from `0` to `100` |
| `human_ratio` | Human contribution ratio | Integer from `0` to `100`, and together with `ai_ratio` must equal `100` |
| `ai_roles` | AI roles | Concrete tasks handled by AI |
| `human_roles` | Human roles | Concrete tasks handled by humans |

### Example

```json
{
  "version": "1.0",
  "ai_ratio": 35,
  "human_ratio": 65,
  "ai_roles": [
    "outline drafting",
    "language polishing",
    "title suggestions"
  ],
  "human_roles": [
    "topic selection",
    "argument design",
    "fact review",
    "final approval"
  ],
  "note": "Voluntary self-disclosure by the author."
}
```

### Display Rules

1. The declaration should appear at the beginning of the article, page, or post
2. It should not be hidden in footnotes, collapsed areas, or low-visibility sections
3. It should not use misleading wording
4. If a card image is used, a text version is still recommended

## Quick Start

### Online Generator

- Direct link: [https://wwenj.github.io/ai-content-transparency/generator/index.html](https://wwenj.github.io/ai-content-transparency/generator/index.html)

### Usage Steps

1. Enter the AI ratio and human ratio
2. Generate and export the declaration card
3. Place the card or text declaration at the beginning of the content

## Preview Examples

![Example 1](./examples/example1.png)

![Example 2](./examples/example2.png)

## Use Cases

- blog posts
- paid knowledge content
- technical documentation
- research notes
- curated information articles
- creator long-form posts

## Open Source

- License: [MIT](./LICENSE)
- Generator: [generator/index.html](./generator/index.html)

