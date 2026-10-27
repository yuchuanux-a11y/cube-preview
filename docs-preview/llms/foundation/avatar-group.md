# AvatarGroup

Display a stacked or grid group of avatars with overflow counting

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { AvatarGroup } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `color` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | 否 | `—` | Color applied to child Avatars (and the overflow count) when they omit color. |
| `isGrid` | `boolean` | 否 | `—` | — |
| `max` | `number` | 否 | `—` | Maximum number of avatar children to render. Omit to show all children (no truncation). |
| `overlap` | `"clip" \| "ring"` | 否 | `"clip"` | How stacked avatars overlap visually. - `"clip"` — crescent mask (transparent seam; no box-shadow) - `"ring"` — solid box-shadow outline via `--background` Has no effect when `isGrid` is true. |
| `render` | `DOMRenderFunction<E, undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `"md"` | Size applied to child Avatars (and the overflow count) when they omit size. Defaults to `md` to stay in sync with Avatar. |
| `variant` | `"default" \| "soft"` | 否 | `—` | Variant applied to child Avatars (and the overflow count) when they omit variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | 否 | `—` | — |

## Parts

- `AvatarGroup.Count`
