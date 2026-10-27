# Spinner

A loading indicator component to show pending states

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Spinner } from "@heroui/react";
```

## Figma

[Open Spinner in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-71607)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `className` | `string` | No | `—` | — |
| `color` | `"current" \| "danger" \| "accent" \| "success" \| "warning"` | No | `—` | Spinner color. |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `size` | `"md" \| "lg" \| "sm" \| "xl"` | No | `—` | Spinner size. |
| `children` | `JSX.IntrinsicElements[E]["children"]` | No | `—` | — |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Example source

```tsx
'use client';

import {Spinner} from "@heroui/react";

export function SpinnerBasic() {
  return (
    <div className="flex items-center gap-4">
      <Spinner />
    </div>
  );
}

export { SpinnerBasic as Preview };
```
