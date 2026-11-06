# Form

Wrapper component for form validation and submission handling

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Form } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | 否 | `—` | The children of the component. |
| `className` | `string` | 否 | `'react-aria-Form'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. |
| `render` | `DOMRenderFunction<"form", undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `style` | `React.CSSProperties` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. |
| `validationBehavior` | `"native" \| "aria"` | 否 | `'native'` | Whether to use native HTML form validation to prevent form submission when a field value is missing or invalid, or mark fields as required or invalid via ARIA. |
