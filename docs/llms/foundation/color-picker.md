# ColorPicker

A composable color picker that synchronizes color value between multiple color components

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { ColorPicker } from "@heroui/react";
```

## Figma

[Open ColorPicker in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=18553-86417)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | Yes | `—` | Content of the color picker (Trigger, Popover, etc.) |
| `className` | `string` | No | `—` | Additional class name for the wrapper element |
| `defaultValue` | `string \| Color` | No | `—` | The default value (uncontrolled). |
| `onChange` | `(value: Color) => void` | No | `—` | Handler that is called when the value changes. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `value` | `string \| Color` | No | `—` | The current value (controlled). |

## Parts

- `ColorPicker.Popover`
- `ColorPicker.Trigger`

## Example source

```tsx
'use client';

import {ColorArea, ColorPicker, ColorSlider, ColorSwatch, Label} from "@heroui/react";

export function Basic() {
  return (
    <ColorPicker defaultValue="#0485F7">
      <ColorPicker.Trigger>
        <ColorSwatch size="lg" />
        <Label>Pick a color</Label>
      </ColorPicker.Trigger>
      <ColorPicker.Popover>
        <ColorArea
          aria-label="Color area"
          className="max-w-full"
          colorSpace="hsb"
          xChannel="saturation"
          yChannel="brightness"
        >
          <ColorArea.Thumb />
        </ColorArea>
        <ColorSlider channel="hue" className="gap-1 px-1" colorSpace="hsb">
          <Label>Hue</Label>
          <ColorSlider.Output className="text-muted" />
          <ColorSlider.Track>
            <ColorSlider.Thumb />
          </ColorSlider.Track>
        </ColorSlider>
      </ColorPicker.Popover>
    </ColorPicker>
  );
}

export { Basic as Preview };
```
