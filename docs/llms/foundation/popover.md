# Popover

Displays rich content in a portal triggered by a button or any custom element

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Popover } from "@heroui/react";
```

## Figma

[Open Popover in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=6192-4931)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | Yes | `—` | — |
| `defaultOpen` | `boolean` | No | `—` | Whether the overlay is open by default (uncontrolled). |
| `isOpen` | `boolean` | No | `—` | Whether the overlay is open by default (controlled). |
| `onOpenChange` | `(isOpen: boolean) => void` | No | `—` | Handler that is called when the overlay's open state changes. |

## Parts

- `Popover.Arrow`
- `Popover.Content`
- `Popover.Dialog`
- `Popover.Heading`
- `Popover.Trigger`

## Example source

```tsx
'use client';

import {Avatar, Button, Popover} from "@heroui/react";
import {useState} from "react";

export function PopoverInteractive() {
  const [isFollowing, setIsFollowing] = useState(false);

  return (
    <div className="flex items-center gap-6">
      <Popover>
        <Popover.Trigger aria-label="User profile">
          <div className="flex items-center gap-2">
            <Avatar size="sm">
              <Avatar.Image
                alt="Sarah Johnson"
                src="https://img.heroui.chat/image/avatar?w=400&h=400&u=1"
              />
              <Avatar.Fallback>SJ</Avatar.Fallback>
            </Avatar>
            <div className="flex flex-col">
              <p className="text-sm font-medium">Sarah Johnson</p>
              <p className="text-xs text-muted">@sarahj</p>
            </div>
          </div>
        </Popover.Trigger>
        <Popover.Content className="w-[320px]">
          <Popover.Dialog>
            <Popover.Heading>
              <div className="flex items-center justify-between">
                <div className="flex items-center gap-3">
                  <Avatar size="md">
                    <Avatar.Image
                      alt="Sarah Johnson"
                      src="https://img.heroui.chat/image/avatar?w=400&h=400&u=1"
                    />
                    <Avatar.Fallback>SJ</Avatar.Fallback>
                  </Avatar>
                  <div>
                    <p className="font-semibold">Sarah Johnson</p>
                    <p className="text-sm text-muted">@sarahj</p>
                  </div>
                </div>
                <Button
                  className="rounded-full"
                  size="sm"
                  variant={isFollowing ? "tertiary" : "primary"}
                  onPress={() => setIsFollowing(!isFollowing)}
                >
                  {isFollowing ? "Following" : "Follow"}
                </Button>
              </div>
            </Popover.Heading>
            <p className="mt-3 text-sm text-muted">
              Product designer and creative director. Building beautiful experiences that matter.
            </p>
            <div className="mt-3 flex gap-4">
              <div>
                <span className="font-semibold">892</span>
                <span className="ms-1 text-sm text-muted">Following</span>
              </div>
              <div>
                <span className="font-semibold">12.5K</span>
                <span className="ms-1 text-sm text-muted">Followers</span>
              </div>
            </div>
          </Popover.Dialog>
        </Popover.Content>
      </Popover>
    </div>
  );
}

export { PopoverInteractive as Preview };
```
