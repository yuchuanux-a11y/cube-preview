# CellSlider

Cube component `CellSlider` from `@bosagent/cube-ui/cell-slider`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/cell-slider` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/cell-slider` |

检索：CellSlider、cell-slider。

## Import

```tsx
import { CellSlider } from "@bosagent/cube-ui/cell-slider";
import { CellSlider } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## 适用

建设中。设计 registry 没有这条用法。

## 不适用

建设中。

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `variant` | `"default" \| "secondary"` | No | `"default"` | Visual variant. |
| `children` | `ChildrenOrFunction<SliderRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<SliderRenderProps>` | No | `'react-aria-Slider'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `number \| number[]` | No | `—` | The default value (uncontrolled). |
| `formatOptions` | `Intl.NumberFormatOptions` | No | `—` | The display format of the value label. |
| `isDisabled` | `boolean` | No | `—` | Whether the whole Slider is disabled. |
| `maxValue` | `number` | No | `100` | The slider's maximum value. |
| `minValue` | `number` | No | `0` | The slider's minimum value. |
| `onChange` | `(value: number \| number[]) => void` | No | `—` | Handler that is called when the value changes. |
| `onChangeEnd` | `(value: number \| number[]) => void` | No | `—` | Fired when the slider stops moving, due to being let go. |
| `render` | `DOMRenderFunction<"div", SliderRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `step` | `number` | No | `1` | The slider's step value. |
| `style` | `StyleOrFunction<SliderRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `number \| number[]` | No | `—` | The current value (controlled). |

## Parts

- `CellSlider.Fill`
- `CellSlider.Label`
- `CellSlider.Output`
- `CellSlider.Thumb`
- `CellSlider.Track`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[CellSlider](https://yuchuanux-a11y.github.io/cube-preview/#CellSlider)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/cell-slider.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { CellSlider } from '@components/cell-slider';

export function Default() {
  return (
    <div className="w-[252px]">
      <CellSlider
        aria-label="Spacing"
        defaultValue={0.5}
        formatOptions={{ maximumFractionDigits: 2, minimumFractionDigits: 2 }}
        maxValue={1}
        minValue={0}
        step={0.01}
      >
        <CellSlider.Track>
          <CellSlider.Fill />
          <CellSlider.Thumb />
          <CellSlider.Label>Spacing</CellSlider.Label>
          <CellSlider.Output />
        </CellSlider.Track>
      </CellSlider>
    </div>
  );
}
```
