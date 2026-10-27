# FieldError

Displays validation error messages for form fields

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { FieldError } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ChildrenOrFunction<FieldErrorRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<FieldErrorRenderProps>` | 否 | `'react-aria-FieldError'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `elementType` | `string` | 否 | `'span'` | The HTML element type to render. Defaults to `'span'`. Set to `'div'` when using block-level children (e.g. `<ul>`) to avoid invalid HTML. |
| `render` | `DOMRenderFunction<"div", FieldErrorRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `style` | `StyleOrFunction<FieldErrorRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/FieldError
