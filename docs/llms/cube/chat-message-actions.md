# ChatMessageActions

Cube component `ChatMessageActions` from `@bosagent/cube-ui/chat-message-actions`.

Cube component. Source: `packages/cube-ui/src/components/chat-message-actions`.

## Import

```tsx
import { ChatMessageActions } from "@bosagent/cube-ui/chat-message-actions";
import { ChatMessageActions } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
