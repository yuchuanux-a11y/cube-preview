# TextArea

Primitive multiline text input component that accepts standard HTML attributes

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { TextArea } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | 否 | `—` | — |
| `variant` | `"primary" \| "secondary"` | 否 | `—` | — |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `ClassNameOrFunction<InputRenderProps>` | 否 | `'react-aria-TextArea'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `render` | `DOMRenderFunction<"textarea", InputRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | — |
| `style` | `StyleOrFunction<InputRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onHoverChange` | `(isHovering: boolean) => void` | 否 | `—` | Handler that is called when the hover state changes. |
| `onHoverEnd` | `(e: HoverEvent) => void` | 否 | `—` | Handler that is called when a hover interaction ends. |
| `onHoverStart` | `(e: HoverEvent) => void` | 否 | `—` | Handler that is called when a hover interaction starts. |

</details>

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-35712

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/TextArea
