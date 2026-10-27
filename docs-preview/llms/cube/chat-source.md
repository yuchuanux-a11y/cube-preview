# ChatSource

Cube component `ChatSource` from `@bosagent/cube-ui/chat-source`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/chat-source` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/chat-source` |

检索：ChatSource、chat-source。

## Import

```tsx
import { ChatSource } from "@bosagent/cube-ui/chat-source";
import { ChatSource } from "@bosagent/cube-ui";
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
| `children` | `ReactNode` | No | `—` | — |
| `description` | `string` | No | `—` | — |
| `enablePreview` | `boolean` | No | `—` | Controls the hover preview for URL sources. By default, preview is enabled when a URL source has a title or description. Set to `true` for custom preview content. |
| `faviconUrl` | `string` | No | `—` | — |
| `href` | `string` | No | `—` | — |
| `sourceType` | `ChatSourceType` | No | `—` | — |
| `title` | `string` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `ChatSource.DocumentIcon`
- `ChatSource.Icon`
- `ChatSource.Preview`
- `ChatSource.Title`
- `ChatSource.Trigger`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ChatSource](https://yuchuanux-a11y.github.io/cube-preview/#ChatSource)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/chat-source.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import type { ReactNode } from 'react';
import { ChatMessage } from '@components/chat-message';
import { ChatSource, ChatSources } from '@components/chat-source';

function getFaviconUrl(href: string): string {
  return `https://www.google.com/s2/favicons?domain_url=${encodeURIComponent(href)}&sz=64`;
}

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
        Here is an answer backed by a single web source.
      </ChatMessage.Content>
      <ChatSource
        description="Cube UI ships presentation-only AI chat compounds for React."
        faviconUrl={getFaviconUrl('https://heroui.com')}
        href="https://heroui.com"
        title="Cube UI"
      />
    </AssistantMessage>
  );
}

export function Document() {
  return (
    <AssistantMessage>
      <ChatMessage.Content>
        Referenced an uploaded document.
      </ChatMessage.Content>
      <ChatSource sourceType="document" title="Q3-launch-brief.pdf" />
    </AssistantMessage>
  );
}

export function Grouped() {
  return (
    <AssistantMessage>
      <ChatMessage.Content>
        Answer synthesized from multiple sources.
      </ChatMessage.Content>
      <ChatSources defaultExpanded={false}>
        <ChatSources.Trigger>3 sources</ChatSources.Trigger>
        <ChatSources.Content>
          <ChatSources.List>
            <ChatSource
              faviconUrl={getFaviconUrl('https://heroui.com')}
              href="https://heroui.com"
              title="HeroUI"
            />
            <ChatSource
              description="Tailwind Variants powers slot-based styling in Pro components."
              faviconUrl={getFaviconUrl('https://tailwind-variants.org')}
              href="https://tailwind-variants.org"
              title="Tailwind Variants"
            />
            <ChatSource sourceType="document" title="design-system-audit.pdf" />
          </ChatSources.List>
        </ChatSources.Content>
      </ChatSources>
    </AssistantMessage>
  );
}

export function Composable() {
  return (
    <AssistantMessage>
      <ChatMessage.Content>
        React&apos;s documentation has a clear explanation of component
        composition and state-driven rendering. The source chip below uses
        custom trigger content with a fetched favicon.
      </ChatMessage.Content>
      <ChatSource enablePreview href="https://react.dev">
        <ChatSource.Trigger>
          <ChatSource.Icon faviconUrl={getFaviconUrl('https://react.dev')} />
          <ChatSource.Title>React docs</ChatSource.Title>
        </ChatSource.Trigger>
        <ChatSource.Preview>
          <div className="flex max-w-72 flex-col gap-2">
            <div className="flex items-center gap-2">
              <ChatSource.Icon
                faviconUrl={getFaviconUrl('https://react.dev')}
              />
              <span className="text-sm font-medium text-foreground">
                react.dev
              </span>
            </div>
            <p className="text-sm text-muted">
              Official React documentation for learning modern React patterns.
            </p>
          </div>
        </ChatSource.Preview>
      </ChatSource>
    </AssistantMessage>
  );
}

export function StackedFavicons() {
  const sources = [
    { href: 'https://www.reuters.com', label: 'Reuters' },
    { href: 'https://nypost.com', label: 'New York Post' },
    { href: 'https://www.foxsports.com', label: 'Fox Sports' },
  ];

  return (
    <AssistantMessage>
      <ChatMessage.Content>
        Answer synthesized from multiple sources.
      </ChatMessage.Content>
      <ChatSources defaultExpanded={false}>
        <ChatSources.Trigger>
          <span className="inline-flex -space-x-1.5">
            {sources.map((source) => (
              <img
                key={source.href}
                alt=""
                className="size-5 rounded-full border border-background object-cover"
                src={getFaviconUrl(source.href)}
              />
            ))}
          </span>
          <span>Sources</span>
        </ChatSources.Trigger>
        <ChatSources.Content>
          <ChatSources.List>
            {sources.map((source) => (
              <ChatSource
                key={source.href}
                faviconUrl={getFaviconUrl(source.href)}
                href={source.href}
                title={source.label}
              />
            ))}
          </ChatSources.List>
        </ChatSources.Content>
      </ChatSources>
    </AssistantMessage>
  );
}
```
