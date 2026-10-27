# Slider

A slider allows a user to select one or more values within a range

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：Slider、slider。

Native 目录说明：以连续刻度调整数值。

## Import

```tsx
import { Slider } from "@heroui/react";
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
| `children` | `ChildrenOrFunction<SliderRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<SliderRenderProps>` | No | `'react-aria-Slider'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `number \| number[]` | No | `—` | The default value (uncontrolled). |
| `formatOptions` | `Intl.NumberFormatOptions` | No | `—` | The display format of the value label. |
| `isDisabled` | `boolean` | No | `—` | Whether the whole Slider is disabled. |
| `maxValue` | `number` | No | `100` | The slider's maximum value. |
| `minValue` | `number` | No | `0` | The slider's minimum value. |
| `onChange` | `(value: number \| number[]) => void` | No | `—` | Handler that is called when the value changes. |
| `onChangeEnd` | `(value: number \| number[]) => void` | No | `—` | Fired when the slider stops moving, due to being let go. |
| `orientation` | `Orientation` | No | `'horizontal'` | The orientation of the Slider. |
| `render` | `DOMRenderFunction<"div", SliderRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `step` | `number` | No | `1` | The slider's step value. |
| `style` | `StyleOrFunction<SliderRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `number \| number[]` | No | `—` | The current value (controlled). |

## Parts

- `Slider.Fill`
- `Slider.Marks`
- `Slider.Output`
- `Slider.Thumb`
- `Slider.Track`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open Slider in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-69689)

## 画廊

[Slider](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Slider)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/slider.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Label, Slider} from "@heroui/react";

export function Default() {
  return (
    <Slider className="w-full max-w-xs" defaultValue={30}>
      <Label>Volume</Label>
      <Slider.Output />
      <Slider.Track>
        <Slider.Fill />
        <Slider.Thumb />
      </Slider.Track>
    </Slider>
  );
}

export { Default as Preview };
```
