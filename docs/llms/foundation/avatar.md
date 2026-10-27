# Avatar

Display user profile images with customizable fallback content

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Avatar } from "@heroui/react";
```

## Figma

[Open Avatar in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-71386)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `color` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `variant` | `"default" \| "soft"` | No | `—` | — |
| `asChild` | `boolean` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `Avatar.Fallback`
- `Avatar.Image`

## Example source

```tsx
'use client';

import {Avatar} from "@heroui/react";

export function Basic() {
  return (
    <div className="flex items-center gap-4">
      <Avatar>
        <Avatar.Image alt="John Doe" src="https://img.heroui.chat/image/avatar?w=400&h=400&u=3" />
        <Avatar.Fallback>JD</Avatar.Fallback>
      </Avatar>
      <Avatar>
        <Avatar.Image
          alt="Blue"
          src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/blue.jpg"
        />
        <Avatar.Fallback>B</Avatar.Fallback>
      </Avatar>
      <Avatar>
        <Avatar.Fallback>JR</Avatar.Fallback>
      </Avatar>
    </div>
  );
}

export { Basic as Preview };
```
