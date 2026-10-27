# Breadcrumbs

Navigation breadcrumbs showing the current page's location within a hierarchy

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Breadcrumbs } from "@heroui/react";
```

## Figma

[Open Breadcrumbs in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=14153-3704)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `separator` | `React.ReactNode` | No | `—` | — |
| `children` | `React.ReactNode \| ((item: unknown) => ReactNode)` | No | `—` | The contents of the collection. |
| `className` | `string` | No | `'react-aria-Breadcrumbs'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. |
| `dependencies` | `readonly any[]` | No | `—` | Values that should invalidate the item cache when using dynamic collections. |
| `isDisabled` | `boolean` | No | `—` | Whether the breadcrumbs are disabled. |
| `items` | `Iterable<unknown>` | No | `—` | Item objects in the collection. |
| `onAction` | `(key: Key) => void` | No | `—` | Handler that is called when a breadcrumb is clicked. |
| `render` | `DOMRenderFunction<"ol", undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `React.CSSProperties` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. |

## Parts

- `Breadcrumbs.Item`

## Example source

```tsx
'use client';

import {Breadcrumbs} from "@heroui/react";

export function Preview() {
  return (
    <Breadcrumbs>
      <Breadcrumbs.Item href="#">Home</Breadcrumbs.Item>
      <Breadcrumbs.Item href="#">Products</Breadcrumbs.Item>
      <Breadcrumbs.Item href="#">Electronics</Breadcrumbs.Item>
      <Breadcrumbs.Item>Laptop</Breadcrumbs.Item>
    </Breadcrumbs>
  );
}
```
