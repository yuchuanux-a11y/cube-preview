# ItemCard

Cube component `ItemCard` from `@bosagent/cube-ui/item-card`.

Cube component. Source: `packages/cube-ui/src/components/item-card`.

## Import

```tsx
import { ItemCard } from "@bosagent/cube-ui/item-card";
import { ItemCard } from "@bosagent/cube-ui";
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
| `variant` | `"outline" \| "default" \| "secondary" \| "tertiary" \| "transparent"` | No | `"default"` | Visual variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Parts

- `ItemCard.Action`
- `ItemCard.Content`
- `ItemCard.Description`
- `ItemCard.Icon`
- `ItemCard.Title`

## Example source

```tsx
'use client';

import { ItemCard } from '@components/item-card';
import { CircleChevronRight, Globe } from '@gravity-ui/icons';
import { Button } from '@heroui/react';

export function Default() {
  return (
    <div className="w-[500px] rounded-2xl p-6">
      <ItemCard>
        <ItemCard.Icon>
          <Globe />
        </ItemCard.Icon>
        <ItemCard.Content>
          <ItemCard.Title>Language</ItemCard.Title>
          <ItemCard.Description>
            Choose your preferred language
          </ItemCard.Description>
        </ItemCard.Content>
        <ItemCard.Action>
          <Button size="sm" variant="outline">
            English
            <CircleChevronRight className="size-3.5" />
          </Button>
        </ItemCard.Action>
      </ItemCard>
    </div>
  );
}
```
