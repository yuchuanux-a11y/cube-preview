# Timeline

Cube component `Timeline` from `@bosagent/cube-ui/timeline`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/timeline` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/timeline` |

检索：Timeline、timeline。

## Import

```tsx
import { Timeline } from "@bosagent/cube-ui/timeline";
import { Timeline } from "@bosagent/cube-ui";
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
| `children` | `React.ReactNode` | Yes | `—` | — |
| `axis` | `"center" \| "start"` | No | `"start"` | Position of the timeline axis. |
| `density` | `"compact" \| "comfortable"` | No | `"comfortable"` | Vertical rhythm between events. |
| `itemAlign` | `"center" \| "start"` | No | `"start"` | Default vertical alignment for item content. |
| `placement` | `TimelinePlacement` | No | `"end"` | Default content side for items. `alternate` alternates start/end by index. |
| `size` | `"md" \| "lg" \| "sm"` | No | `"md"` | Size variant. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `Timeline.Connector`
- `Timeline.Content`
- `Timeline.Item`
- `Timeline.Marker`
- `Timeline.Rail`
- `Timeline.useItem`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[Timeline](https://yuchuanux-a11y.github.io/cube-preview/#Timeline)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/timeline.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { Timeline } from '@components/timeline';
import { Check, Clock, Code, Rocket } from '@gravity-ui/icons';

const events = [
  {
    description: 'Design tokens and component anatomy are approved.',
    icon: Check,
    status: 'success' as const,
    title: 'Foundation locked',
  },
  {
    description:
      'Rich text editor, timeline, and layout updates are in review.',
    icon: Code,
    status: 'current' as const,
    title: 'Beta 6 source sync',
  },
  {
    description: 'Examples and release checks are queued for final validation.',
    icon: Clock,
    status: 'warning' as const,
    title: 'Verification pass',
  },
  {
    description: 'Ship the updated package and publish component docs.',
    icon: Rocket,
    status: 'default' as const,
    title: 'Release',
  },
];

export function Default() {
  return (
    <Timeline axis="center" className="w-full max-w-3xl" placement="alternate">
      {events.map((event) => (
        <Timeline.Item key={event.title} status={event.status}>
          <Timeline.Marker>
            <event.icon className="size-4" />
          </Timeline.Marker>
          <Timeline.Content>
            <h3 className="text-sm font-semibold text-foreground">
              {event.title}
            </h3>
            <p className="mt-1 text-sm text-muted">{event.description}</p>
          </Timeline.Content>
        </Timeline.Item>
      ))}
    </Timeline>
  );
}
```
