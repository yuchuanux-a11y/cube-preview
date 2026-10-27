# FloatingToc

Cube component `FloatingToc` from `@bosagent/cube-ui/floating-toc`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/floating-toc` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/floating-toc` |

检索：FloatingToc、floating-toc。

## Import

```tsx
import { FloatingToc } from "@bosagent/cube-ui/floating-toc";
import { FloatingToc } from "@bosagent/cube-ui";
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
| `closeDelay` | `number` | No | `300` | Time in ms before the floating toc closes after pointer/focus leave. |
| `defaultOpen` | `boolean` | No | `—` | Default open state (uncontrolled). |
| `onOpenChange` | `(open: boolean) => void` | No | `—` | Callback when open state changes. |
| `open` | `boolean` | No | `—` | Controlled open state. |
| `openDelay` | `number` | No | `200` | Time in ms before the floating toc opens after hover. |
| `placement` | `"left" \| "right"` | No | `"right"` | Which side of the page the TOC is on. Controls bar growth direction and default content side. |
| `triggerMode` | `"hover" \| "press"` | No | `"hover"` | How the trigger opens the content. |

## Parts

- `FloatingToc.Bar`
- `FloatingToc.Content`
- `FloatingToc.Item`
- `FloatingToc.Trigger`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[FloatingToc](https://yuchuanux-a11y.github.io/cube-preview/#FloatingToc)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/floating-toc.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { useState } from 'react';
import { FloatingToc } from '@components/floating-toc';

const tocItems = [
  { id: 'overview', label: 'Overview' },
  { id: 'installation', label: 'Installation' },
  { id: 'quick-start', label: 'Quick start' },
  { id: 'configuration', label: 'Configuration' },
  { id: 'api-reference', label: 'API reference' },
  { id: 'troubleshooting', label: 'Troubleshooting' },
];

export function Default() {
  const [activeId, setActiveId] = useState('overview');

  return (
    <div className="px-10 py-24">
      <FloatingToc>
        <FloatingToc.Trigger aria-label="Table of contents">
          {tocItems.map((item) => (
            <FloatingToc.Bar key={item.id} active={item.id === activeId} />
          ))}
        </FloatingToc.Trigger>
        <FloatingToc.Content>
          {tocItems.map((item) => (
            <FloatingToc.Item
              key={item.id}
              active={item.id === activeId}
              onClick={() => setActiveId(item.id)}
            >
              {item.label}
            </FloatingToc.Item>
          ))}
        </FloatingToc.Content>
      </FloatingToc>
    </div>
  );
}
```
