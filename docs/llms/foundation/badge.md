# Badge

Displays a small indicator positioned relative to another element, commonly used for notification counts, status dots, and labels

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Badge } from "@heroui/react";
```

## Figma

[Open Badge in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=19865-36040)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `color` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | No | `—` | Badge color. |
| `placement` | `"bottom-right" \| "bottom-left" \| "top-left" \| "top-right"` | No | `—` | Badge placement. |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | Badge size. |
| `variant` | `"primary" \| "secondary" \| "soft"` | No | `—` | Badge variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Parts

- `Badge.Anchor`
- `Badge.Label`

## Example source

```tsx
'use client';

import {Avatar, Badge} from "@heroui/react";

const GREEN_AVATAR_URL = "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/green.jpg";
const ORANGE_AVATAR_URL =
  "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/orange.jpg";
const BLUE_AVATAR_URL = "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/blue.jpg";

export function BadgeBasic() {
  return (
    <div className="flex items-center gap-6">
      <Badge.Anchor>
        <Avatar>
          <Avatar.Image src={GREEN_AVATAR_URL} />
          <Avatar.Fallback>JD</Avatar.Fallback>
        </Avatar>
        <Badge color="danger" size="sm">
          5
        </Badge>
      </Badge.Anchor>

      <Badge.Anchor>
        <Avatar>
          <Avatar.Image src={ORANGE_AVATAR_URL} />
          <Avatar.Fallback>AB</Avatar.Fallback>
        </Avatar>
        <Badge color="accent" size="sm">
          New
        </Badge>
      </Badge.Anchor>

      <Badge.Anchor>
        <Avatar>
          <Avatar.Image src={BLUE_AVATAR_URL} />
          <Avatar.Fallback>CD</Avatar.Fallback>
        </Avatar>
        <Badge color="success" placement="bottom-right" size="sm" />
      </Badge.Anchor>
    </div>
  );
}

export { BadgeBasic as Preview };
```
