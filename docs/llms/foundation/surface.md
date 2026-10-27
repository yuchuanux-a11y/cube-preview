# Surface

Container component that provides surface-level styling and context for child components

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Surface } from "@heroui/react";
```

## Figma

[Open Surface in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17294-52295)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `variant` | `"default" \| "secondary" \| "tertiary" \| "transparent"` | No | `"default"` | Visual variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Example source

```tsx
'use client';

import {Surface} from "@heroui/react";

export function Basic() {
  return (
    <Surface className="flex min-w-[320px] flex-col gap-3 rounded-3xl p-6" variant="default">
      <h3 className="text-base font-semibold text-foreground">Surface Content</h3>
      <p className="text-sm text-muted">
        This is a default surface variant. It uses bg-surface styling.
      </p>
    </Surface>
  );
}

export { Basic as Preview };
```
