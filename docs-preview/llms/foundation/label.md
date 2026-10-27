# Label

Renders an accessible label associated with form controls

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Label } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `isDisabled` | `boolean` | 否 | `—` | — |
| `isInvalid` | `boolean` | 否 | `—` | — |
| `isRequired` | `boolean` | 否 | `—` | — |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `elementType` | `string` | 否 | `—` | — |
| `render` | `DOMRenderFunction<"label", undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | — |

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-33325

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Label
