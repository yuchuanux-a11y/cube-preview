# ColorSwatchPicker

A list of color swatches that allows users to select a color from a predefined palette.

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { ColorSwatchPicker } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `size` | `"md" \| "lg" \| "sm" \| "xl" \| "xs"` | 否 | `—` | — |
| `variant` | `"circle" \| "square"` | 否 | `—` | — |
| `children` | `React.ReactNode` | 否 | `—` | The children of the ColorSwatchPicker. |
| `className` | `ClassNameOrFunction<ColorSwatchPickerRenderProps>` | 否 | `'react-aria-ColorSwatchPicker'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `string \| Color` | 否 | `—` | The default value (uncontrolled). |
| `layout` | `"grid" \| "stack"` | 否 | `'grid'` | Whether the items are arranged in a stack or grid. |
| `render` | `DOMRenderFunction<"div", ColorSwatchPickerRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `style` | `StyleOrFunction<ColorSwatchPickerRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `string \| Color` | 否 | `—` | The current value (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onChange` | `(value: Color) => void` | 否 | `—` | Handler that is called when the value changes. |

</details>

## Parts

- `ColorSwatchPicker.Indicator`
- `ColorSwatchPicker.Item`
- `ColorSwatchPicker.Swatch`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=18411-2327
