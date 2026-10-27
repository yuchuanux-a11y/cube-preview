# Chip

Small informational badges for displaying labels, statuses, and categories

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Chip } from "@heroui/react";
```

## Figma

[Open Chip in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-71211)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `color` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | No | `—` | Chip color. |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | Chip size. |
| `variant` | `"primary" \| "secondary" \| "tertiary" \| "soft"` | No | `—` | Chip variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Parts

- `Chip.Label`

## Example source

```tsx
'use client';

import {Chip} from "@heroui/react";

export function ChipBasic() {
  return (
    <div className="flex flex-wrap items-center gap-3">
      <Chip>Default</Chip>
      <Chip color="accent">Accent</Chip>
      <Chip color="success">Success</Chip>
      <Chip color="warning">Warning</Chip>
      <Chip color="danger">Danger</Chip>
    </div>
  );
}

export { ChipBasic as Preview };
```
