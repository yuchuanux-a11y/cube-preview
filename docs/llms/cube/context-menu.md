# ContextMenu

Cube component `ContextMenu` from `@bosagent/cube-ui/context-menu`.

Cube component. Source: `packages/cube-ui/src/components/context-menu`.

## Import

```tsx
import { ContextMenu } from "@bosagent/cube-ui/context-menu";
import { ContextMenu } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `defaultOpen` | `boolean` | No | `—` | Default open state (uncontrolled). |
| `isDisabled` | `boolean` | No | `—` | Whether the context menu is disabled. |
| `onOpenChange` | `(open: boolean) => void` | No | `—` | Callback when open state changes. |
| `open` | `boolean` | No | `—` | Controlled open state. |

## Parts

- `ContextMenu.Item`
- `ContextMenu.ItemIndicator`
- `ContextMenu.Menu`
- `ContextMenu.Popover`
- `ContextMenu.Section`
- `ContextMenu.Separator`
- `ContextMenu.SubmenuIndicator`
- `ContextMenu.SubmenuTrigger`
- `ContextMenu.Trigger`

## Example source

```tsx
'use client';

import { ContextMenu } from '@components/context-menu';
import { Kbd, Label } from '@heroui/react';

export function Default() {
  return (
    <ContextMenu>
      <ContextMenu.Trigger>
        <div className="flex h-48 w-80 items-center justify-center rounded-xl border border-dashed border-border text-sm text-muted select-none">
          Right-click here
        </div>
      </ContextMenu.Trigger>
      <ContextMenu.Popover>
        <ContextMenu.Menu>
          <ContextMenu.Item id="back" textValue="Back">
            <Label>Back</Label>
            <Kbd className="ms-auto" slot="keyboard" variant="light">
              <Kbd.Abbr keyValue="command" />
              <Kbd.Content>[</Kbd.Content>
            </Kbd>
          </ContextMenu.Item>
          <ContextMenu.Item isDisabled id="forward" textValue="Forward">
            <Label>Forward</Label>
            <Kbd className="ms-auto" slot="keyboard" variant="light">
              <Kbd.Abbr keyValue="command" />
              <Kbd.Content>]</Kbd.Content>
            </Kbd>
          </ContextMenu.Item>
          <ContextMenu.Item id="reload" textValue="Reload">
            <Label>Reload</Label>
            <Kbd className="ms-auto" slot="keyboard" variant="light">
              <Kbd.Abbr keyValue="command" />
              <Kbd.Content>R</Kbd.Content>
            </Kbd>
          </ContextMenu.Item>
          <ContextMenu.Separator />
          <ContextMenu.Item id="view-source" textValue="View Page Source">
            <Label>View Page Source</Label>
          </ContextMenu.Item>
          <ContextMenu.Item id="inspect" textValue="Inspect">
            <Label>Inspect</Label>
          </ContextMenu.Item>
        </ContextMenu.Menu>
      </ContextMenu.Popover>
    </ContextMenu>
  );
}
```
