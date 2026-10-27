# ProgressCircle

A circular progress indicator that shows determinate or indeterminate progress.

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { ProgressCircle } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `color` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | 否 | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | — |
| `children` | `ChildrenOrFunction<ProgressBarRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ProgressBarRenderProps>` | 否 | `'react-aria-ProgressBar'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `formatOptions` | `Intl.NumberFormatOptions` | 否 | `{ style: 'percent' }` | The display format of the value label. |
| `isIndeterminate` | `boolean` | 否 | `—` | Whether presentation is indeterminate when progress isn't known. |
| `maxValue` | `number` | 否 | `100` | The largest value allowed for the input. |
| `minValue` | `number` | 否 | `0` | The smallest value allowed for the input. |
| `render` | `DOMRenderFunction<"div", ProgressBarRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ProgressBarRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `number` | 否 | `0` | The current value (controlled). |
| `valueLabel` | `ReactNode` | 否 | `—` | The content to display as the value's label (e.g. 1 of 4). |

## Parts

- `ProgressCircle.FillCircle`
- `ProgressCircle.Track`
- `ProgressCircle.TrackCircle`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=21302-79204
