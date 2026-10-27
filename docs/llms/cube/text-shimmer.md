# TextShimmer

Cube component `TextShimmer` from `@bosagent/cube-ui/text-shimmer`.

Cube component. Source: `packages/cube-ui/src/components/text-shimmer`.

## Import

```tsx
import { TextShimmer } from "@bosagent/cube-ui/text-shimmer";
import { TextShimmer } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Example source

```tsx
'use client';

import { TextShimmer } from '@components/text-shimmer';

export function Default() {
  return (
    <div className="flex flex-col gap-4 text-sm">
      <TextShimmer>Thinking...</TextShimmer>
      <TextShimmer>Generating response...</TextShimmer>
    </div>
  );
}
```
