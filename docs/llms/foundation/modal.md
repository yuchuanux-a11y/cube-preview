# Modal

Dialog overlay for focused user interactions and important content

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Modal } from "@heroui/react";
```

## Figma

[Open Modal in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-77858)

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

- `Modal.Backdrop`
- `Modal.Body`
- `Modal.CloseTrigger`
- `Modal.Container`
- `Modal.Dialog`
- `Modal.Footer`
- `Modal.Header`
- `Modal.Heading`
- `Modal.Icon`
- `Modal.Trigger`

## Example source

```tsx
'use client';

import {Rocket} from "@gravity-ui/icons";
import {Button, Modal} from "@heroui/react";

export function Default() {
  return (
    <Modal>
      <Button variant="secondary">Open Modal</Button>
      <Modal.Backdrop>
        <Modal.Container>
          <Modal.Dialog className="sm:max-w-[360px]">
            <Modal.CloseTrigger />
            <Modal.Header>
              <Modal.Icon className="bg-default text-foreground">
                <Rocket className="size-5" />
              </Modal.Icon>
              <Modal.Heading>Welcome to HeroUI</Modal.Heading>
            </Modal.Header>
            <Modal.Body>
              <p>
                A beautiful, fast, and modern React UI library for building accessible and
                customizable web applications with ease.
              </p>
            </Modal.Body>
            <Modal.Footer>
              <Button className="w-full" slot="close">
                Continue
              </Button>
            </Modal.Footer>
          </Modal.Dialog>
        </Modal.Container>
      </Modal.Backdrop>
    </Modal>
  );
}

export { Default as Preview };
```
