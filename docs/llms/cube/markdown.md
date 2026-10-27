# Markdown

Cube component `Markdown` from `@bosagent/cube-ui/markdown`.

Cube component. Source: `packages/cube-ui/src/components/markdown`.

## Import

```tsx
import { Markdown } from "@bosagent/cube-ui/markdown";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `string` | Yes | `—` | — |
| `components` | `Partial<Components>` | No | `—` | — |
| `id` | `string` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Example source

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
