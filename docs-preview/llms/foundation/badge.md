# Badge

Displays a small indicator positioned relative to another element, commonly used for notification counts, status dots, and labels

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Badge } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `color` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | 否 | `—` | Badge color. |
| `placement` | `"bottom-right" \| "bottom-left" \| "top-left" \| "top-right"` | 否 | `—` | Badge placement. |
| `render` | `DOMRenderFunction<E, undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | Badge size. |
| `variant` | `"primary" \| "secondary" \| "soft"` | 否 | `—` | Badge variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | 否 | `—` | — |

## Parts

- `Badge.Anchor`
- `Badge.Label`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=19865-36040
