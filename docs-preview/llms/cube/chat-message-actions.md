# ChatMessageActions

Cube component `ChatMessageActions` from `@bosagent/cube-ui/chat-message-actions`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/chat-message-actions` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/chat-message-actions` |

检索：ChatMessageActions、chat-message-actions。

## Import

```tsx
import { ChatMessageActions } from "@bosagent/cube-ui/chat-message-actions";
import { ChatMessageActions } from "@bosagent/cube-ui";
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
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `ChatMessageActions.CopiedIcon`
- `ChatMessageActions.Copy`
- `ChatMessageActions.CopyIcon`
- `ChatMessageActions.Menu`
- `ChatMessageActions.MenuIcon`
- `ChatMessageActions.Regenerate`
- `ChatMessageActions.RegenerateIcon`
- `ChatMessageActions.ThumbsDown`
- `ChatMessageActions.ThumbsDownIcon`
- `ChatMessageActions.ThumbsUp`
- `ChatMessageActions.ThumbsUpIcon`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ChatMessageActions](https://yuchuanux-a11y.github.io/cube-preview/#ChatMessageActions)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/chat-message-actions.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import type { ReactNode } from 'react';
import { ChatMessage } from '@components/chat-message';
import { ChatMessageActions } from '@components/chat-message-actions';
import { Copy, ThumbsUp } from '@gravity-ui/icons';

function AssistantMessage({ children }: { children: ReactNode }) {
  return (
    <ChatMessage.Assistant>
      <ChatMessage.Avatar show alt="Assistant" fallback="AI" />
      <ChatMessage.Body>{children}</ChatMessage.Body>
    </ChatMessage.Assistant>
  );
}

export function Default() {
  return (
    <AssistantMessage>
      <ChatMessage.Content>
        Assistant responses can expose quick actions beneath the message body.
      </ChatMessage.Content>
      <ChatMessageActions>
        <ChatMessageActions.Copy aria-label="Copy" tooltip="Copy" />
        <ChatMessageActions.ThumbsUp
          aria-label="Good response"
          tooltip="Good response"
        />
        <ChatMessageActions.ThumbsDown
          aria-label="Bad response"
          tooltip="Bad response"
        />
        <ChatMessageActions.Regenerate
          aria-label="Regenerate"
          tooltip="Regenerate"
        />
        <ChatMessageActions.Menu aria-label="More actions" tooltip="More" />
      </ChatMessageActions>
    </AssistantMessage>
  );
}

export function Minimal() {
  return (
    <AssistantMessage>
      <ChatMessage.Content>
        Minimal action set for compact layouts.
      </ChatMessage.Content>
      <ChatMessageActions>
        <ChatMessageActions.Copy aria-label="Copy" tooltip="Copy" />
        <ChatMessageActions.Menu aria-label="More actions" tooltip="More" />
      </ChatMessageActions>
    </AssistantMessage>
  );
}

export function CustomIcons() {
  return (
    <AssistantMessage>
      <ChatMessage.Content>
        Swap preset icons via the Icon subcomponents.
      </ChatMessage.Content>
      <ChatMessageActions>
        <ChatMessageActions.Copy aria-label="Copy" tooltip="Copy">
          <ChatMessageActions.CopyIcon>
            <Copy className="size-4 text-accent" />
          </ChatMessageActions.CopyIcon>
        </ChatMessageActions.Copy>
        <ChatMessageActions.ThumbsUp
          aria-label="Good response"
          tooltip="Good response"
        >
          <ChatMessageActions.ThumbsUpIcon>
            <ThumbsUp className="size-4 text-success" />
          </ChatMessageActions.ThumbsUpIcon>
        </ChatMessageActions.ThumbsUp>
      </ChatMessageActions>
    </AssistantMessage>
  );
}
```
