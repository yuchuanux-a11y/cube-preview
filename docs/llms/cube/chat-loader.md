# ChatLoader

Cube component `ChatLoader` from `@bosagent/cube-ui/chat-loader`.

Cube component. Source: `packages/cube-ui/src/components/chat-loader`.

## Import

```tsx
import { ChatLoader } from "@bosagent/cube-ui/chat-loader";
import { ChatLoader } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
