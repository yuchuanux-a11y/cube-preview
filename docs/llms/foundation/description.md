# Description

Provides supplementary text for form fields and other components

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Description } from "@heroui/react";
```

## Figma

[Open Description in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17290-25455)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `elementType` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<any, any>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | — |

## Example source

```tsx
'use client';

import {Description, Input, Label} from "@heroui/react";

export function Basic() {
  return (
    <div className="flex flex-col gap-1">
      <Label htmlFor="email">Email</Label>
      <Input
        aria-describedby="email-description"
        className="w-64"
        id="email"
        placeholder="you@example.com"
        type="email"
      />
      <Description id="email-description">
        We'll never share your email with anyone else.
      </Description>
    </div>
  );
}

export { Basic as Preview };
```
