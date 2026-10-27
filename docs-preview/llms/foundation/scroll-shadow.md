# ScrollShadow

Apply visual shadows to indicate scrollable content overflow with automatic detection of scroll position.

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { ScrollShadow } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `hideScrollBar` | `boolean` | 否 | `—` | — |
| `isEnabled` | `boolean` | 否 | `true` | Whether scroll shadow detection is enabled |
| `offset` | `number` | 否 | `0` | The scroll offset before showing shadows (in pixels) |
| `orientation` | `"horizontal" \| "vertical"` | 否 | `—` | — |
| `size` | `number` | 否 | `40` | The shadow size in pixels |
| `variant` | `"fade"` | 否 | `—` | — |
| `visibility` | `ScrollShadowVisibility` | 否 | `"auto"` | Controlled shadow visibility state |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onVisibilityChange` | `(visibility: ScrollShadowVisibility) => void` | 否 | `—` | Callback invoked when shadow visibility changes |

</details>

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-73776

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/ScrollShadow
