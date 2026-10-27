# TrendChip

Cube component `TrendChip` from `@bosagent/cube-ui/trend-chip`.

Cube component. Source: `packages/cube-ui/src/components/trend-chip`.

## Import

```tsx
import { TrendChip } from "@bosagent/cube-ui/trend-chip";
import { TrendChip } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<keyof React.JSX.IntrinsicElements, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `trend` | `TrendType` | No | `—` | — |
| `variant` | `"primary" \| "secondary" \| "tertiary" \| "soft"` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `TrendChip.Indicator`
- `TrendChip.Prefix`
- `TrendChip.Suffix`

## Example source

```tsx
'use client';

import { TrendChip } from '@components/trend-chip';

export function Default() {
  return (
    <div className="flex items-center gap-3 rounded-2xl p-6">
      <TrendChip trend="up">+3.3%</TrendChip>
      <TrendChip trend="down">-2.1%</TrendChip>
      <TrendChip trend="neutral">0.0%</TrendChip>
    </div>
  );
}
```
