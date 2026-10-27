# CellSlider

Cube component `CellSlider` from `@bosagent/cube-ui/cell-slider`.

- 分层：Cube
- 包：`@bosagent/cube-ui/cell-slider`
- 状态：建设中

## Import

```tsx
import { CellSlider } from "@bosagent/cube-ui/cell-slider";
import { CellSlider } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `variant` | `"default" \| "secondary"` | 否 | `"default"` | Visual variant. |
| `children` | `ChildrenOrFunction<SliderRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<SliderRenderProps>` | 否 | `'react-aria-Slider'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `number \| number[]` | 否 | `—` | The default value (uncontrolled). |
| `formatOptions` | `Intl.NumberFormatOptions` | 否 | `—` | The display format of the value label. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the whole Slider is disabled. |
| `maxValue` | `number` | 否 | `100` | The slider's maximum value. |
| `minValue` | `number` | 否 | `0` | The slider's minimum value. |
| `render` | `DOMRenderFunction<"div", SliderRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `step` | `number` | 否 | `1` | The slider's step value. |
| `style` | `StyleOrFunction<SliderRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `number \| number[]` | 否 | `—` | The current value (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onChange` | `(value: number \| number[]) => void` | 否 | `—` | Handler that is called when the value changes. |
| `onChangeEnd` | `(value: number \| number[]) => void` | 否 | `—` | Fired when the slider stops moving, due to being let go. |

</details>

## Parts

- `CellSlider.Fill`
- `CellSlider.Label`
- `CellSlider.Output`
- `CellSlider.Thumb`
- `CellSlider.Track`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#CellSlider
