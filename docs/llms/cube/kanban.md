# Kanban

Cube component `Kanban` from `@bosagent/cube-ui/kanban`.

Cube component. Source: `packages/cube-ui/src/components/kanban`.

## Import

```tsx
import { Kanban } from "@bosagent/cube-ui/kanban";
import { Kanban } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `hideScrollBar` | `boolean` | No | `—` | — |
| `isEnabled` | `boolean` | No | `true` | Whether scroll shadow detection is enabled |
| `offset` | `number` | No | `0` | The scroll offset before showing shadows (in pixels) |
| `onVisibilityChange` | `(visibility: ScrollShadowVisibility) => void` | No | `—` | Callback invoked when shadow visibility changes |
| `orientation` | `"horizontal" \| "vertical"` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `"md"` | Size variant controlling card padding, font size, and column width. |
| `variant` | `"fade"` | No | `—` | — |
| `visibility` | `ScrollShadowVisibility` | No | `"auto"` | Controlled shadow visibility state |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `Kanban.Card`
- `Kanban.CardList`
- `Kanban.Column`
- `Kanban.ColumnActions`
- `Kanban.ColumnBody`
- `Kanban.ColumnCount`
- `Kanban.ColumnHeader`
- `Kanban.ColumnIndicator`
- `Kanban.ColumnTitle`
- `Kanban.DragHandle`
- `Kanban.DropIndicator`
- `Kanban.ScrollShadow`

## Example source

```tsx
'use client';

import { Kanban } from '@components/kanban';

const columns = [
  {
    id: 'todo',
    title: 'Todo',
    cards: ['Prepare demo', 'Review API'],
  },
  {
    id: 'doing',
    title: 'In Progress',
    cards: ['Wire preview'],
  },
  {
    id: 'done',
    title: 'Done',
    cards: ['Create catalog'],
  },
];

export function Default() {
  return (
    <Kanban className="max-w-full">
      {columns.map((column) => (
        <Kanban.Column key={column.id}>
          <Kanban.ColumnHeader>
            <Kanban.ColumnIndicator />
            <Kanban.ColumnTitle>{column.title}</Kanban.ColumnTitle>
            <Kanban.ColumnCount>{column.cards.length}</Kanban.ColumnCount>
          </Kanban.ColumnHeader>
          <Kanban.ColumnBody>
            <Kanban.CardList aria-label={`${column.title} tasks`}>
              {column.cards.map((card) => (
                <Kanban.Card
                  id={`${column.id}-${card}`}
                  key={card}
                  textValue={card}
                >
                  {card}
                </Kanban.Card>
              ))}
            </Kanban.CardList>
          </Kanban.ColumnBody>
        </Kanban.Column>
      ))}
    </Kanban>
  );
}
```
