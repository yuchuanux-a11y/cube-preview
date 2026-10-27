# NativeSelect

Cube component `NativeSelect` from `@bosagent/cube-ui/native-select`.

Cube component. Source: `packages/cube-ui/src/components/native-select`.

## Import

```tsx
import { NativeSelect } from "@bosagent/cube-ui/native-select";
import { NativeSelect } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `fullWidth` | `boolean` | No | `—` | Whether the select should take up the full width of its container. |
| `variant` | `"primary" \| "secondary"` | No | `"primary"` | The visual variant. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `NativeSelect.Indicator`
- `NativeSelect.OptGroup`
- `NativeSelect.Option`
- `NativeSelect.Trigger`

## Example source

```tsx
'use client';

import { NativeSelect } from '@components/native-select';

export function Default() {
  return (
    <div className="w-full max-w-[220px]">
      <NativeSelect className="w-full">
        <NativeSelect.Trigger>
          <NativeSelect.Option value="">Select status</NativeSelect.Option>
          <NativeSelect.Option value="todo">Todo</NativeSelect.Option>
          <NativeSelect.Option value="in-progress">
            In Progress
          </NativeSelect.Option>
          <NativeSelect.Option value="done">Done</NativeSelect.Option>
          <NativeSelect.Option value="cancelled">Cancelled</NativeSelect.Option>
          <NativeSelect.Indicator />
        </NativeSelect.Trigger>
      </NativeSelect>
    </div>
  );
}
```
