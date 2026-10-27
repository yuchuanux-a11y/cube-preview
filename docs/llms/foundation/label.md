# Label

Renders an accessible label associated with form controls

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Label } from "@heroui/react";
```

## Figma

[Open Label in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-33325)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `isDisabled` | `boolean` | No | `—` | — |
| `isInvalid` | `boolean` | No | `—` | — |
| `isRequired` | `boolean` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `elementType` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<"label", undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | — |

## Example source

```tsx
'use client';

import {Input, Label} from "@heroui/react";

export function Basic() {
  return (
    <div className="flex flex-col gap-1">
      <Label htmlFor="name">Name</Label>
      <Input className="w-64" id="name" placeholder="Enter your name" type="text" />
    </div>
  );
}

export { Basic as Preview };
```
