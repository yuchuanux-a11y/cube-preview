# Separator

Visually divide content sections

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Separator } from "@heroui/react";
```

## Figma

[Open Separator in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-70816)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `variant` | `"default" \| "secondary" \| "tertiary"` | No | `—` | — |
| `className` | `string` | No | `'react-aria-Separator'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. |
| `elementType` | `string` | No | `—` | The HTML element type that will be used to render the separator. |
| `orientation` | `Orientation` | No | `'horizontal'` | The orientation of the separator. |
| `render` | `DOMRenderFunction<"div" \| "hr", undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `React.CSSProperties` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. |

## Example source

```tsx
'use client';

import {Separator} from "@heroui/react";

export function Basic() {
  return (
    <div className="max-w-md">
      <div className="space-y-1">
        <h4 className="text-medium font-medium">HeroUI v3 Components</h4>
        <p className="text-small text-default-400">Beautiful, fast and modern React UI library.</p>
      </div>
      <Separator className="my-4" />
      <div className="text-small flex h-5 items-center space-x-4">
        <div>Blog</div>
        <Separator orientation="vertical" />
        <div>Docs</div>
        <Separator orientation="vertical" />
        <div>Source</div>
      </div>
    </div>
  );
}

export { Basic as Preview };
```
