# EmptyState

Cube component `EmptyState` from `@bosagent/cube-ui/empty-state`.

Cube component. Source: `packages/cube-ui/src/components/empty-state`.

## Import

```tsx
import { EmptyState } from "@bosagent/cube-ui/empty-state";
import { EmptyState } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `size` | `"md" \| "lg" \| "sm"` | No | `"md"` | Size variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Parts

- `EmptyState.Content`
- `EmptyState.Description`
- `EmptyState.Header`
- `EmptyState.Media`
- `EmptyState.Title`

## Example source

```tsx
'use client';

import { EmptyState } from '@components/empty-state';
import { FolderOpen } from '@gravity-ui/icons';
import { Button } from '@heroui/react';

export function Default() {
  return (
    <div className="w-[420px]">
      <EmptyState>
        <EmptyState.Header>
          <EmptyState.Media variant="icon">
            <FolderOpen />
          </EmptyState.Media>
          <EmptyState.Title>No Projects Yet</EmptyState.Title>
          <EmptyState.Description>
            You haven&apos;t created any projects yet. Get started by creating
            your first project.
          </EmptyState.Description>
        </EmptyState.Header>
        <EmptyState.Content className="flex-row gap-2">
          <Button>Create Project</Button>
          <Button variant="outline">Import Project</Button>
        </EmptyState.Content>
      </EmptyState>
    </div>
  );
}
```
