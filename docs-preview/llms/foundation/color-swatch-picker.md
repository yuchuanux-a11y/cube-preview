# ColorSwatchPicker

A list of color swatches that allows users to select a color from a predefined palette.

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：ColorSwatchPicker、color-swatch-picker。

## Import

```tsx
import { ColorSwatchPicker } from "@heroui/react";
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
| `size` | `"md" \| "lg" \| "sm" \| "xl" \| "xs"` | No | `—` | — |
| `variant` | `"circle" \| "square"` | No | `—` | — |
| `children` | `React.ReactNode` | No | `—` | The children of the ColorSwatchPicker. |
| `className` | `ClassNameOrFunction<ColorSwatchPickerRenderProps>` | No | `'react-aria-ColorSwatchPicker'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `string \| Color` | No | `—` | The default value (uncontrolled). |
| `layout` | `"grid" \| "stack"` | No | `'grid'` | Whether the items are arranged in a stack or grid. |
| `onChange` | `(value: Color) => void` | No | `—` | Handler that is called when the value changes. |
| `render` | `DOMRenderFunction<"div", ColorSwatchPickerRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `style` | `StyleOrFunction<ColorSwatchPickerRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `string \| Color` | No | `—` | The current value (controlled). |

## Parts

- `ColorSwatchPicker.Indicator`
- `ColorSwatchPicker.Item`
- `ColorSwatchPicker.Swatch`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open ColorSwatchPicker in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=18411-2327)

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/color-swatch-picker.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {ColorSwatchPicker} from "@heroui/react";

const colors = ["#F43F5E", "#D946EF", "#8B5CF6", "#3B82F6", "#06B6D4", "#10B981", "#84CC16"];

export function Basic() {
  return (
    <ColorSwatchPicker>
      {colors.map((color) => (
        <ColorSwatchPicker.Item key={color} color={color}>
          <ColorSwatchPicker.Swatch />
          <ColorSwatchPicker.Indicator />
        </ColorSwatchPicker.Item>
      ))}
    </ColorSwatchPicker>
  );
}

export { Basic as Preview };
```
