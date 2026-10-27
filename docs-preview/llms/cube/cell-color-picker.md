# CellColorPicker

Cube component `CellColorPicker` from `@bosagent/cube-ui/cell-color-picker`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/cell-color-picker` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/cell-color-picker` |

检索：CellColorPicker、cell-color-picker。

## Import

```tsx
import { CellColorPicker } from "@bosagent/cube-ui/cell-color-picker";
import { CellColorPicker } from "@bosagent/cube-ui";
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
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `variant` | `"default" \| "secondary"` | No | `"default"` | Visual variant. |
| `defaultValue` | `string \| Color` | No | `—` | The default value (uncontrolled). |
| `onChange` | `(value: Color) => void` | No | `—` | Handler that is called when the value changes. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `value` | `string \| Color` | No | `—` | The current value (controlled). |

## Parts

- `CellColorPicker.Label`
- `CellColorPicker.Popover`
- `CellColorPicker.Swatch`
- `CellColorPicker.Trigger`
- `CellColorPicker.ValueDisplay`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[CellColorPicker](https://yuchuanux-a11y.github.io/cube-preview/#CellColorPicker)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/cell-color-picker.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { CellColorPicker } from '@components/cell-color-picker';
import { ColorArea, ColorSlider, Label } from '@heroui/react';

export function Default() {
  return (
    <div className="w-[252px]">
      <CellColorPicker aria-label="Accent" defaultValue="#3B82F6">
        <CellColorPicker.Trigger>
          <CellColorPicker.Label>Accent</CellColorPicker.Label>
          <CellColorPicker.ValueDisplay />
          <CellColorPicker.Swatch />
        </CellColorPicker.Trigger>
        <CellColorPicker.Popover>
          <ColorArea
            aria-label="Color area"
            className="max-w-full"
            colorSpace="hsb"
            xChannel="saturation"
            yChannel="brightness"
          >
            <ColorArea.Thumb />
          </ColorArea>
          <ColorSlider
            aria-label="Hue"
            channel="hue"
            className="gap-1 px-1"
            colorSpace="hsb"
          >
            <Label>Hue</Label>
            <ColorSlider.Output className="text-muted" />
            <ColorSlider.Track>
              <ColorSlider.Thumb />
            </ColorSlider.Track>
          </ColorSlider>
        </CellColorPicker.Popover>
      </CellColorPicker>
    </div>
  );
}
```
