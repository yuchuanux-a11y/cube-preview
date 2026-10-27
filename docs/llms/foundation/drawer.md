# Drawer

Slide-out panel for supplementary content and actions

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Drawer } from "@heroui/react";
```

## Figma

[Open Drawer in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=21149-43114)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `state` | `UseOverlayStateReturn` | No | `—` | — |
| `children` | `React.ReactNode` | Yes | `—` | — |
| `defaultOpen` | `boolean` | No | `—` | Whether the overlay is open by default (uncontrolled). |
| `isOpen` | `boolean` | No | `—` | Whether the overlay is open by default (controlled). |
| `onOpenChange` | `(isOpen: boolean) => void` | No | `—` | Handler that is called when the overlay's open state changes. |

## Parts

- `Drawer.Backdrop`
- `Drawer.Body`
- `Drawer.CloseTrigger`
- `Drawer.Content`
- `Drawer.Dialog`
- `Drawer.Footer`
- `Drawer.Handle`
- `Drawer.Header`
- `Drawer.Heading`
- `Drawer.Trigger`

## Example source

```tsx
'use client';

import {Button, Drawer} from "@heroui/react";

export function Basic() {
  return (
    <Drawer>
      <Button variant="secondary">Open Drawer</Button>
      <Drawer.Backdrop>
        <Drawer.Content placement="right">
          <Drawer.Dialog>
            <Drawer.Header>
              <Drawer.Heading>Drawer Title</Drawer.Heading>
            </Drawer.Header>
            <Drawer.Body>
              <p>
                This is a bottom drawer built with React Aria's Modal component. It slides up from
                the bottom of the screen with a smooth CSS transition.
              </p>
            </Drawer.Body>
            <Drawer.Footer>
              <Button slot="close" variant="secondary">
                Cancel
              </Button>
              <Button slot="close">Confirm</Button>
            </Drawer.Footer>
          </Drawer.Dialog>
        </Drawer.Content>
      </Drawer.Backdrop>
    </Drawer>
  );
}

export { Basic as Preview };
```
