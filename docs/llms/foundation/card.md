# Card

Flexible container component for grouping related content and actions

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Card } from "@heroui/react";
```

## Figma

[Open Card in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-72791)

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

## Parts

- `Card.Content`
- `Card.Description`
- `Card.Footer`
- `Card.Header`
- `Card.Title`

## Example source

```tsx
'use client';

import {CircleDollar} from "@gravity-ui/icons";
import {Card, Link} from "@heroui/react";

export function Default() {
  return (
    <Card className="w-[400px]">
      <CircleDollar aria-label="Dollar sign icon" className="text-primary size-6" role="img" />
      <Card.Header>
        <Card.Title>Become an Acme Creator!</Card.Title>
        <Card.Description>
          Visit the Acme Creator Hub to sign up today and start earning credits from your fans and
          followers.
        </Card.Description>
      </Card.Header>
      <Card.Footer>
        <Link
          aria-label="Go to Acme Creator Hub (opens in new tab)"
          href="https://heroui.com"
          rel="noopener noreferrer"
          target="_blank"
        >
          Creator Hub
          <Link.Icon aria-hidden="true" />
        </Link>
      </Card.Footer>
    </Card>
  );
}

export { Default as Preview };
```
