# Skeleton

Skeleton is a placeholder to show a loading state and the expected shape of a component.

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Skeleton } from "@heroui/react";
```

## Figma

[Open Skeleton in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=6141-14118)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `animationType` | `"none" \| "pulse" \| "shimmer"` | No | `—` | Animation type. |
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `children` | `JSX.IntrinsicElements[E]["children"]` | No | `—` | — |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Example source

```tsx
'use client';

import {Skeleton} from "@heroui/react";

export function Basic() {
  return (
    <div className="shadow-panel w-[250px] space-y-5 rounded-lg bg-transparent p-4">
      <Skeleton className="h-32 rounded-lg" />
      <div className="space-y-3">
        <Skeleton className="h-3 w-3/5 rounded-lg" />
        <Skeleton className="h-3 w-4/5 rounded-lg" />
        <Skeleton className="h-3 w-2/5 rounded-lg" />
      </div>
    </div>
  );
}

export { Basic as Preview };
```
