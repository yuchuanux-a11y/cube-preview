# CellColorPicker

Cube component `CellColorPicker` from `@bosagent/cube-ui/cell-color-picker`.

Cube component. Source: `packages/cube-ui/src/components/cell-color-picker`.

## Import

```tsx
import { CellColorPicker } from "@bosagent/cube-ui/cell-color-picker";
import { CellColorPicker } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
