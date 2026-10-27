# ColorSwatch

A visual preview of a color value with accessibility support

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { ColorSwatch } from "@heroui/react";
```

## Figma

[Open ColorSwatch in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=18408-5727)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `shape` | `"circle" \| "square"` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm" \| "xl" \| "xs"` | No | `—` | — |
| `className` | `ClassNameOrFunction<ColorSwatchRenderProps>` | No | `'react-aria-ColorSwatch'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `color` | `string \| Color` | No | `—` | The color value to display in the swatch. |
| `colorName` | `string` | No | `—` | A localized accessible name for the color. By default, a description is generated from the color value, but this can be overridden if you have a more specific color name (e.g. Pantone colors). |
| `render` | `DOMRenderFunction<"div", ColorSwatchRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ColorSwatchRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Example source

```tsx
'use client';

import {ColorSwatch} from "@heroui/react";

export function ColorSwatchBasic() {
  return (
    <div className="flex items-center gap-3">
      <ColorSwatch aria-label="Blue" color="#0485F7" />
      <ColorSwatch aria-label="Red" color="#EF4444" />
      <ColorSwatch aria-label="Amber" color="#F59E0B" />
      <ColorSwatch aria-label="Green" color="#10B981" />
      <ColorSwatch aria-label="Fuchsia" color="#D946EF" />
    </div>
  );
}

export { ColorSwatchBasic as Preview };
```
