# PressableFeedback

Cube component `PressableFeedback` from `@bosagent/cube-ui/pressable-feedback`.

Cube component. Source: `packages/cube-ui/src/components/pressable-feedback`.

## Import

```tsx
import { PressableFeedback } from "@bosagent/cube-ui/pressable-feedback";
import { PressableFeedback } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `isDisabled` | `boolean` | No | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Parts

- `PressableFeedback.Highlight`
- `PressableFeedback.HoldConfirm`
- `PressableFeedback.ProgressFeedback`
- `PressableFeedback.Ripple`

## Example source

```tsx
'use client';

import { PressableFeedback } from '@components/pressable-feedback';
import {
  Ellipsis,
  Envelope,
  Gear,
  Globe,
  Plus,
  TrashBin,
} from '@gravity-ui/icons';
import { Button } from '@heroui/react';

export function Default() {
  return (
    <div className="flex flex-col gap-6">
      <div className="flex flex-wrap gap-3">
        <Button>
          <PressableFeedback.Ripple />
          Primary
        </Button>
        <Button variant="secondary">
          <PressableFeedback.Ripple />
          Secondary
        </Button>
        <Button variant="tertiary">
          <PressableFeedback.Ripple />
          Tertiary
        </Button>
        <Button variant="outline">
          <PressableFeedback.Ripple />
          Outline
        </Button>
        <Button variant="ghost">
          <PressableFeedback.Ripple />
          Ghost
        </Button>
        <Button variant="danger">
          <PressableFeedback.Ripple />
          Danger
        </Button>
      </div>

      <div className="flex flex-wrap gap-3">
        <Button>
          <PressableFeedback.Ripple />
          <Globe />
          Search
        </Button>
        <Button variant="secondary">
          <PressableFeedback.Ripple />
          <Plus />
          Add Member
        </Button>
        <Button variant="tertiary">
          <PressableFeedback.Ripple />
          <Envelope />
          Email
        </Button>
        <Button variant="danger">
          <PressableFeedback.Ripple />
          <TrashBin />
          Delete
        </Button>
      </div>

      <div className="flex gap-3">
        <Button isIconOnly variant="tertiary">
          <PressableFeedback.Ripple />
          <Ellipsis />
        </Button>
        <Button isIconOnly variant="secondary">
          <PressableFeedback.Ripple />
          <Gear />
        </Button>
        <Button isIconOnly variant="danger">
          <PressableFeedback.Ripple />
          <TrashBin />
        </Button>
      </div>
    </div>
  );
}
```
