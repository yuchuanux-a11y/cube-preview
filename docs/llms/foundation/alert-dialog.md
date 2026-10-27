# AlertDialog

Modal dialog for critical confirmations requiring user attention and explicit action

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { AlertDialog } from "@heroui/react";
```

## Figma

[Open AlertDialog in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=7814-319)

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

- `AlertDialog.Backdrop`
- `AlertDialog.Body`
- `AlertDialog.CloseTrigger`
- `AlertDialog.Container`
- `AlertDialog.Dialog`
- `AlertDialog.Footer`
- `AlertDialog.Header`
- `AlertDialog.Heading`
- `AlertDialog.Icon`
- `AlertDialog.Trigger`

## Example source

```tsx
'use client';

import {AlertDialog, Button} from "@heroui/react";

export function Default() {
  return (
    <AlertDialog>
      <Button variant="danger">Delete Project</Button>
      <AlertDialog.Backdrop>
        <AlertDialog.Container>
          <AlertDialog.Dialog className="sm:max-w-[400px]">
            <AlertDialog.CloseTrigger />
            <AlertDialog.Header>
              <AlertDialog.Icon status="danger" />
              <AlertDialog.Heading>Delete project permanently?</AlertDialog.Heading>
            </AlertDialog.Header>
            <AlertDialog.Body>
              <p>
                This will permanently delete <strong>My Awesome Project</strong> and all of its
                data. This action cannot be undone.
              </p>
            </AlertDialog.Body>
            <AlertDialog.Footer>
              <Button slot="close" variant="tertiary">
                Cancel
              </Button>
              <Button slot="close" variant="danger">
                Delete Project
              </Button>
            </AlertDialog.Footer>
          </AlertDialog.Dialog>
        </AlertDialog.Container>
      </AlertDialog.Backdrop>
    </AlertDialog>
  );
}

export { Default as Preview };
```
