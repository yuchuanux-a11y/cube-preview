# ActionBar

Cube component `ActionBar` from `@bosagent/cube-ui/action-bar`.

Cube component. Source: `packages/cube-ui/src/components/action-bar`.

## Import

```tsx
import { ActionBar } from "@bosagent/cube-ui/action-bar";
import { ActionBar } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `isOpen` | `boolean` | Yes | `—` | Controls visibility with animated enter/exit. |
| `isAttached` | `boolean` | No | `—` | — |
| `className` | `ClassNameOrFunction<ToolbarRenderProps>` | No | `'react-aria-Toolbar'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `orientation` | `Orientation` | No | `'horizontal'` | The orientation of the entire toolbar. |
| `render` | `DOMRenderFunction<"div", ToolbarRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ToolbarRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `ActionBar.Content`
- `ActionBar.Prefix`
- `ActionBar.Suffix`

## Example source

```tsx
'use client';

import { useState } from 'react';
import type { Selection } from 'react-aria-components/GridList';
import { ActionBar } from '@components/action-bar';
import { ListView } from '@components/list-view';
import {
  Archive,
  ArrowDownToLine,
  Pencil,
  TrashBin,
  Xmark,
} from '@gravity-ui/icons';
import { Button, Chip, Separator, Tooltip } from '@heroui/react';

const items = [
  { id: 1, label: 'Project proposal.pdf' },
  { id: 2, label: 'Q4 financial report.xlsx' },
  { id: 3, label: 'Brand guidelines.fig' },
  { id: 4, label: 'Team photo.jpg' },
  { id: 5, label: 'Meeting notes.md' },
  { id: 6, label: 'API documentation.pdf' },
];

export function Default() {
  const [selected, setSelected] = useState<Selection>(() => new Set());

  const selectionCount =
    selected === 'all' ? items.length : (selected as Set<number>).size;

  return (
    <div className="w-full max-w-lg p-4">
      <ListView
        aria-label="Files"
        items={items}
        selectedKeys={selected}
        selectionMode="multiple"
        variant="primary"
        onSelectionChange={setSelected}
      >
        {(item) => (
          <ListView.Item id={item.id} textValue={item.label}>
            <ListView.ItemContent>
              <ListView.Title>{item.label}</ListView.Title>
            </ListView.ItemContent>
          </ListView.Item>
        )}
      </ListView>

      <ActionBar isOpen={selectionCount > 0}>
        <ActionBar.Prefix>
          <Chip className="shrink-0 tabular-nums" size="sm">
            {selectionCount}
          </Chip>
        </ActionBar.Prefix>
        <Separator />
        <ActionBar.Content>
          <Button aria-label="Edit" size="sm" variant="ghost">
            <Pencil />
            <span className="action-bar__label">Edit</span>
          </Button>
          <Button aria-label="Export" size="sm" variant="ghost">
            <ArrowDownToLine />
            <span className="action-bar__label">Export</span>
          </Button>
          <Button aria-label="Archive" size="sm" variant="ghost">
            <Archive />
            <span className="action-bar__label">Archive</span>
          </Button>
          <Separator orientation="vertical" />
          <Button
            aria-label="Delete"
            className="bg-danger/10 text-danger"
            size="sm"
            variant="ghost"
          >
            <TrashBin />
            <span className="action-bar__label">Delete</span>
          </Button>
        </ActionBar.Content>
        <Separator />
        <ActionBar.Suffix>
          <Tooltip>
            <Button
              isIconOnly
              aria-label="Clear selection"
              size="sm"
              variant="ghost"
              onPress={() => setSelected(new Set())}
            >
              <Xmark />
            </Button>
            <Tooltip.Content>Clear selection</Tooltip.Content>
          </Tooltip>
        </ActionBar.Suffix>
      </ActionBar>
    </div>
  );
}
```
