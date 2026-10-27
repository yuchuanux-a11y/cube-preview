# AvatarGroup

Display a stacked or grid group of avatars with overflow counting

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { AvatarGroup } from "@heroui/react";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `color` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | No | `—` | Color applied to child Avatars (and the overflow count) when they omit color. |
| `isGrid` | `boolean` | No | `—` | — |
| `max` | `number` | No | `—` | Maximum number of avatar children to render. Omit to show all children (no truncation). |
| `overlap` | `"clip" \| "ring"` | No | `"clip"` | How stacked avatars overlap visually. - `"clip"` — crescent mask (transparent seam; no box-shadow) - `"ring"` — solid box-shadow outline via `--background` Has no effect when `isGrid` is true. |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `size` | `"md" \| "lg" \| "sm"` | No | `"md"` | Size applied to child Avatars (and the overflow count) when they omit size. Defaults to `md` to stay in sync with Avatar. |
| `variant` | `"default" \| "soft"` | No | `—` | Variant applied to child Avatars (and the overflow count) when they omit variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Parts

- `AvatarGroup.Count`

## Example source

```tsx
'use client';

import {Avatar, AvatarGroup} from "@heroui/react";

const users = [
  {
    id: 1,
    image: "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/blue.jpg",
    name: "John Doe",
  },
  {
    id: 2,
    image: "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/green.jpg",
    name: "Kate Wilson",
  },
  {
    id: 3,
    image: "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/purple.jpg",
    name: "Emily Chen",
  },
  {
    id: 4,
    image: "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/orange.jpg",
    name: "Michael Brown",
  },
  {
    id: 5,
    image: "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/red.jpg",
    name: "Olivia Davis",
  },
];

export function Basic() {
  return (
    <AvatarGroup>
      {users.slice(0, 4).map((user) => (
        <Avatar key={user.id}>
          <Avatar.Image alt={user.name} src={user.image} />
          <Avatar.Fallback>
            {user.name
              .split(" ")
              .map((n) => n[0])
              .join("")}
          </Avatar.Fallback>
        </Avatar>
      ))}
    </AvatarGroup>
  );
}

export { Basic as Preview };
```
