# Skeleton

Skeleton is a placeholder to show a loading state and the expected shape of a component.

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Skeleton } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `animationType` | `"none" \| "pulse" \| "shimmer"` | 否 | `—` | Animation type. |
| `className` | `string` | 否 | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `children` | `JSX.IntrinsicElements[E]["children"]` | 否 | `—` | — |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | 否 | `—` | — |

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=6141-14118

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Skeleton
