# ColorArea

A 2D color picker that allows users to select colors from a gradient area

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { ColorArea } from "@heroui/react";
```

## Figma

[Open ColorArea in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=18514-47954)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `showDots` | `boolean` | No | `—` | — |
| `children` | `ChildrenOrFunction<ColorAreaRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ColorAreaRenderProps>` | No | `'react-aria-ColorArea'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `colorSpace` | `ColorSpace` | No | `—` | The color space that the color area operates in. The `xChannel` and `yChannel` must be in this color space. If not provided, this defaults to the color space of the `color` or `defaultColor` value. |
| `defaultValue` | `string \| Color` | No | `—` | The default value (uncontrolled). |
| `form` | `string` | No | `—` | The `<form>` element to associate the ColorArea with. The value of this attribute must be the id of a `<form>` in the same document. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/input#form). |
| `isDisabled` | `boolean` | No | `—` | Whether the ColorArea is disabled. |
| `onChange` | `(value: Color) => void` | No | `—` | Handler that is called when the value changes, as the user drags. |
| `onChangeEnd` | `(value: Color) => void` | No | `—` | Handler that is called when the user stops dragging. |
| `render` | `DOMRenderFunction<"div", ColorAreaRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ColorAreaRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `string \| Color` | No | `—` | The current value (controlled). |
| `xChannel` | `ColorChannel` | No | `—` | Color channel for the horizontal axis. |
| `xName` | `string` | No | `—` | The name of the x channel input element, used when submitting an HTML form. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefname). |
| `yChannel` | `ColorChannel` | No | `—` | Color channel for the vertical axis. |
| `yName` | `string` | No | `—` | The name of the y channel input element, used when submitting an HTML form. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefname). |

## Parts

- `ColorArea.Thumb`

## Example source

```tsx
'use client';

import type {Color} from "@heroui/react";

import {ColorArea, ColorSwatch, parseColor} from "@heroui/react";
import {useState} from "react";

export function ColorAreaControlled() {
  const [color, setColor] = useState<Color>(parseColor("#9B80FF"));

  return (
    <div className="flex flex-col gap-4">
      <ColorArea colorSpace="rgb" value={color} xChannel="red" yChannel="green" onChange={setColor}>
        <ColorArea.Thumb />
      </ColorArea>
      <div className="flex w-[300px] items-center gap-3">
        <ColorSwatch color={color} size="md" />
        <p className="text-sm text-muted">
          Current color:{" "}
          <span className="font-medium">{color ? color.toString("hex") : "(empty)"}</span>
        </p>
      </div>
    </div>
  );
}

export { ColorAreaControlled as Preview };
```
