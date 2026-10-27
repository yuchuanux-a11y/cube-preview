# ChatLoader

Cube component `ChatLoader` from `@bosagent/cube-ui/chat-loader`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/chat-loader` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/chat-loader` |

检索：ChatLoader、chat-loader。

## Import

```tsx
import { ChatLoader } from "@bosagent/cube-ui/chat-loader";
import { ChatLoader } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## 适用

建设中。设计 registry 没有这条用法。

## 不适用

建设中。

## Props


### Dots

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `label` | `string` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### Pulse

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `label` | `string` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### Skeleton

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | No | `—` | — |
| `label` | `string` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### SkeletonAvatar

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### SkeletonBlock

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### SkeletonLine

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### Spinner

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `label` | `string` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `ChatLoader.Dots`
- `ChatLoader.Pulse`
- `ChatLoader.Skeleton`
- `ChatLoader.SkeletonAvatar`
- `ChatLoader.SkeletonBlock`
- `ChatLoader.SkeletonLine`
- `ChatLoader.Spinner`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ChatLoader](https://yuchuanux-a11y.github.io/cube-preview/#ChatLoader)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/chat-loader.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { ChatLoader } from '@components/chat-loader';

export function Default() {
  return (
    <div className="flex w-[420px] flex-col gap-8">
      <div className="flex items-center gap-3">
        <span className="text-sm text-muted">Dots</span>
        <ChatLoader.Dots />
      </div>
      <div className="flex items-center gap-3">
        <span className="text-sm text-muted">Pulse</span>
        <ChatLoader.Pulse />
      </div>
      <div className="flex items-center gap-3">
        <span className="text-sm text-muted">Spinner</span>
        <ChatLoader.Spinner />
      </div>
      <ChatLoader.Skeleton />
    </div>
  );
}
```
