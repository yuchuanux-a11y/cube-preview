# Resizable

Cube component `Resizable` from `@bosagent/cube-ui/resizable`.

Cube component. Source: `packages/cube-ui/src/components/resizable`.

## Import

```tsx
import { Resizable } from "@bosagent/cube-ui/resizable";
```

## Figma

[Open Resizable in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=16902-29717)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | Yes | `—` | — |
| `autoSaveId` | `string` | No | `—` | — |
| `handleRef` | `React.Ref<GroupImperativeHandle>` | No | `—` | — |
| `id` | `string` | No | `—` | — |
| `onLayoutChange` | `(layout: Layout) => void` | No | `—` | — |
| `orientation` | `"horizontal" \| "vertical"` | No | `—` | — |
| `storage` | `LayoutStorage` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `Resizable.Handle`
- `Resizable.Indicator`
- `Resizable.Panel`

## Example source

```tsx
'use client';

import { Resizable } from '@components/resizable';

export function Default() {
  return (
    <div className="h-[400px] w-full overflow-hidden rounded-xl border border-border bg-background">
      <Resizable orientation="horizontal">
        <Resizable.Panel defaultSize="240px" maxSize="360px" minSize="180px">
          <div className="flex h-full items-center justify-center p-6">
            <span className="text-sm font-medium">Sidebar</span>
          </div>
        </Resizable.Panel>
        <Resizable.Handle />
        <Resizable.Panel defaultSize="70%" minSize={30}>
          <div className="flex h-full items-center justify-center p-6">
            <span className="text-sm font-medium text-foreground">
              Main content
            </span>
          </div>
        </Resizable.Panel>
      </Resizable>
    </div>
  );
}
```
