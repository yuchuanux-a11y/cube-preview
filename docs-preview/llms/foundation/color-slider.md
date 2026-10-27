# ColorSlider

A color slider allows users to adjust an individual channel of a color value

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：ColorSlider、color-slider。

## Import

```tsx
import { ColorSlider } from "@heroui/react";
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
| `channel` | `HSLChannel` | Yes | `—` | — |
| `colorSpace` | `"hsl"` | No | `—` | — |
| `children` | `ChildrenOrFunction<ColorSliderRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ColorSliderRenderProps>` | No | `'react-aria-ColorSlider'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `string \| Color` | No | `—` | The default value (uncontrolled). |
| `isDisabled` | `boolean` | No | `—` | Whether the whole Slider is disabled. |
| `onChange` | `(value: Color) => void` | No | `—` | Handler that is called when the value changes, as the user drags. |
| `onChangeEnd` | `(value: Color) => void` | No | `—` | Handler that is called when the user stops dragging. |
| `orientation` | `Orientation` | No | `'horizontal'` | The orientation of the Slider. |
| `render` | `DOMRenderFunction<"div", ColorSliderRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ColorSliderRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `string \| Color` | No | `—` | The current value (controlled). |

## Parts

- `ColorSlider.Output`
- `ColorSlider.Thumb`
- `ColorSlider.Track`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open ColorSlider in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=18553-85013)

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/color-slider.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {ColorSlider, Label} from "@heroui/react";

export function Basic() {
  return (
    <ColorSlider channel="hue" className="w-full max-w-xs" defaultValue="hsl(0, 100%, 50%)">
      <Label>Hue</Label>
      <ColorSlider.Output />
      <ColorSlider.Track>
        <ColorSlider.Thumb />
      </ColorSlider.Track>
    </ColorSlider>
  );
}

export { Basic as Preview };
```
