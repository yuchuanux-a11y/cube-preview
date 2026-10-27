# Markdown

Cube component `Markdown` from `@bosagent/cube-ui/markdown`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/markdown` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/markdown` |

检索：Markdown、markdown。

## Import

```tsx
import { Markdown } from "@bosagent/cube-ui/markdown";
```

## Preview

The docs page renders a live preview of the real component.

## 适用

建设中。设计 registry 没有这条用法。

## 不适用

建设中。

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `string` | Yes | `—` | — |
| `components` | `Partial<Components>` | No | `—` | — |
| `id` | `string` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[Markdown](https://yuchuanux-a11y.github.io/cube-preview/#Markdown)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/markdown.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { Markdown } from '@components/markdown';

const SAMPLE = `# Cube UI AI Markdown

This component uses **react-markdown** with block-level memoization for streaming performance.

## Features

- Headings, lists, and links
- Inline \`code\` snippets
- Fenced code blocks with Shiki highlighting

\`\`\`tsx
<ChatMessage.Assistant>
  <ChatMessage.Avatar alt="Assistant" fallback="AI" show />
  <ChatMessage.Body>
    <ChatMessage.Content>
      <Markdown>{response}</Markdown>
    </ChatMessage.Content>
  </ChatMessage.Body>
</ChatMessage.Assistant>
\`\`\`

> AI responses can include rich formatting without coupling to any SDK.
`;

export function Default() {
  return (
    <div className="w-[640px]">
      <Markdown>{SAMPLE}</Markdown>
    </div>
  );
}
```
