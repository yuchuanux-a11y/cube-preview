# Typography

A semantic typography primitive for headings, body copy, and inline code built on React Aria Components Text.

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Typography } from "@heroui/react";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `align` | `TypographyAlign` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `color` | `TypographyColor` | No | `—` | — |
| `truncate` | `boolean` | No | `—` | — |
| `type` | `TypographyType` | No | `—` | — |
| `weight` | `TypographyWeight` | No | `—` | — |
| `render` | `DOMRenderFunction<any, any>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | — |

## Parts

- `Typography.Code`
- `Typography.Heading`
- `Typography.Paragraph`
- `Typography.Prose`

## Example source

```tsx
'use client';

import {Typography} from "@heroui/react";

export const Default = () => {
  return (
    <div className="flex max-w-xl flex-col gap-4">
      <Typography type="h1">Build better interfaces</Typography>
      <Typography type="h2">Typography that stays semantic</Typography>
      <Typography type="h3">Composable by default</Typography>
      <Typography type="h4">Small heading</Typography>
      <Typography>
        HeroUI Typography uses React Aria Components Text as the primitive, with semantic typography
        types and render-prop polymorphism.
      </Typography>
      <Typography color="muted" type="body-sm">
        Smaller muted body copy for secondary descriptions.
      </Typography>
      <Typography type="code">pnpm add @heroui/react</Typography>
    </div>
  );
};

export { Default as Preview };
```
