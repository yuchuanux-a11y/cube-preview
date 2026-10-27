# Table

Tables display structured data in rows and columns with support for sorting, selection, column resizing, and infinite scrolling.

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Table } from "@heroui/react";
```

## Figma

[Open Table in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=18729-23034)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `variant` | `"primary" \| "secondary"` | No | `—` | Visual variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Parts

- `Table.Body`
- `Table.Cell`
- `Table.Collection`
- `Table.Column`
- `Table.ColumnResizer`
- `Table.Content`
- `Table.Footer`
- `Table.Header`
- `Table.LoadMore`
- `Table.LoadMoreContent`
- `Table.ResizableContainer`
- `Table.Row`
- `Table.ScrollContainer`
- `Table.SortableColumnHeader`

## Example source

```tsx
'use client';

import {Table} from "@heroui/react";

export function Basic() {
  return (
    <Table>
      <Table.ScrollContainer>
        <Table.Content aria-label="Team members" className="min-w-[600px]">
          <Table.Header>
            <Table.Column isRowHeader>Name</Table.Column>
            <Table.Column>Role</Table.Column>
            <Table.Column>Status</Table.Column>
            <Table.Column>Email</Table.Column>
          </Table.Header>
          <Table.Body>
            <Table.Row>
              <Table.Cell>Kate Moore</Table.Cell>
              <Table.Cell>CEO</Table.Cell>
              <Table.Cell>Active</Table.Cell>
              <Table.Cell>kate@acme.com</Table.Cell>
            </Table.Row>
            <Table.Row>
              <Table.Cell>John Smith</Table.Cell>
              <Table.Cell>CTO</Table.Cell>
              <Table.Cell>Active</Table.Cell>
              <Table.Cell>john@acme.com</Table.Cell>
            </Table.Row>
            <Table.Row>
              <Table.Cell>Sara Johnson</Table.Cell>
              <Table.Cell>CMO</Table.Cell>
              <Table.Cell>On Leave</Table.Cell>
              <Table.Cell>sara@acme.com</Table.Cell>
            </Table.Row>
            <Table.Row>
              <Table.Cell>Michael Brown</Table.Cell>
              <Table.Cell>CFO</Table.Cell>
              <Table.Cell>Active</Table.Cell>
              <Table.Cell>michael@acme.com</Table.Cell>
            </Table.Row>
          </Table.Body>
        </Table.Content>
      </Table.ScrollContainer>
    </Table>
  );
}

export { Basic as Preview };
```
