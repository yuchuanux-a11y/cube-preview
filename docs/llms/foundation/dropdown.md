# Dropdown

A dropdown displays a list of actions or options that a user can choose

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Dropdown } from "@heroui/react";
```

## Figma

[Open Dropdown in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-70150)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `className` | `string` | No | `—` | — |
| `children` | `React.ReactNode` | Yes | `—` | — |
| `defaultOpen` | `boolean` | No | `—` | Whether the overlay is open by default (uncontrolled). |
| `isOpen` | `boolean` | No | `—` | Whether the overlay is open by default (controlled). |
| `onOpenChange` | `(isOpen: boolean) => void` | No | `—` | Handler that is called when the overlay's open state changes. |
| `trigger` | `MenuTriggerType` | No | `'press'` | How the menu is triggered. |

## Parts

- `Dropdown.Item`
- `Dropdown.ItemIndicator`
- `Dropdown.Menu`
- `Dropdown.Popover`
- `Dropdown.Section`
- `Dropdown.SubmenuIndicator`
- `Dropdown.SubmenuTrigger`
- `Dropdown.Trigger`

## Example source

```tsx
'use client';

import {Button, Dropdown, Label} from "@heroui/react";

export function Default() {
  return (
    <Dropdown>
      <Button aria-label="Menu" variant="secondary">
        Actions
      </Button>
      <Dropdown.Popover>
        <Dropdown.Menu onAction={(key) => console.log(`Selected: ${key}`)}>
          <Dropdown.Item id="new-file" textValue="New file">
            <Label>New file</Label>
          </Dropdown.Item>
          <Dropdown.Item id="copy-link" textValue="Copy link">
            <Label>Copy link</Label>
          </Dropdown.Item>
          <Dropdown.Item id="edit-file" textValue="Edit file">
            <Label>Edit file</Label>
          </Dropdown.Item>
          <Dropdown.Item id="delete-file" textValue="Delete file" variant="danger">
            <Label>Delete file</Label>
          </Dropdown.Item>
        </Dropdown.Menu>
      </Dropdown.Popover>
    </Dropdown>
  );
}

export { Default as Preview };
```
