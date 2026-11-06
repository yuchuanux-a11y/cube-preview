# Typography

A semantic typography primitive for headings, body copy, and inline code built on React Aria Components Text.

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Typography } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `align` | `TypographyAlign` | 否 | `—` | — |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `color` | `TypographyColor` | 否 | `—` | — |
| `truncate` | `boolean` | 否 | `—` | — |
| `type` | `TypographyType` | 否 | `—` | — |
| `weight` | `TypographyWeight` | 否 | `—` | — |
| `render` | `DOMRenderFunction<any, any>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | — |

## Parts

- `Typography.Code`
- `Typography.Heading`
- `Typography.Paragraph`
- `Typography.Prose`
