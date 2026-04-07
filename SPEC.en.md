# AI Content Transparency Specification

[中文](./SPEC.md)

## 1. Scope

This specification defines a minimal disclosure format for AI participation in published content. It is designed for articles, blog posts, newsletters, notes, documentation, and similar text-first media.

## 2. Required Fields

### `ai_ratio`

- Type: integer
- Range: `0` to `100`
- Meaning: estimated percentage of AI contribution to the final published content
- Note: this is a self-reported estimate of contribution to output, not a measure of time spent

### `human_ratio`

- Type: integer
- Range: `0` to `100`
- Meaning: estimated percentage of human contribution to the final published content
- Rule: `ai_ratio + human_ratio = 100`

### `ai_roles`

- Type: array of strings
- Meaning: concrete tasks completed by AI
- Examples: `"outline drafting"`, `"language polishing"`, `"title suggestions"`, `"translation draft"`

### `human_roles`

- Type: array of strings
- Meaning: concrete tasks completed by humans
- Examples: `"topic selection"`, `"argument design"`, `"fact review"`, `"final approval"`

## 3. Rules

1. `ai_ratio` and `human_ratio` must add up to `100`.
2. If `ai_ratio > 0`, `ai_roles` should contain at least one specific role.
3. If `human_ratio > 0`, `human_roles` should contain at least one specific role.
4. Ratios should reflect contribution to the published result, not only drafting time or tool usage frequency.
5. Roles should be concrete and understandable. Avoid vague wording such as `"assisted"` without explanation.

## 4. Example JSON

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

## 5. Display Rules

1. The declaration must appear at the beginning of the article, page, or post.
2. Prefer placing it before the main body, or immediately below the title and metadata.
3. It must be visible and readable. It should not be hidden in footnotes, collapsible blocks, or visually minimized areas.
4. It must not use misleading wording. If AI materially contributed, do not label the content as fully human-made.
5. When a card image is used, the same information should remain clear in text or accessible metadata when possible.
