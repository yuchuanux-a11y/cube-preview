# Table

Tables display structured data in rows and columns with support for sorting, selection, column resizing, and infinite scrolling.

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Table } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `variant` | `"primary" \| "secondary"` | 否 | `—` | Visual variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | 否 | `—` | — |

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

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=18729-23034
