# DataGrid

Cube component `DataGrid` from `@bosagent/cube-ui/data-grid`.

- 分层：Cube
- 包：`@bosagent/cube-ui/data-grid`
- 状态：建设中

## Import

```tsx
import { DataGrid } from "@bosagent/cube-ui/data-grid";
import { DataGrid } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `columns` | `DataGridColumn<T>[]` | 是 | `—` | Column definitions. |
| `data` | `T[]` | 是 | `—` | Row data array. |
| `getRowId` | `(item: T) => string \| number` | 是 | `—` | Extracts a unique key from each row item. |
| `allowsColumnResize` | `boolean` | 否 | `false` | Enable column resizing on columns that opt in. |
| `className` | `string` | 否 | `—` | Additional className for the root wrapper. |
| `contentClassName` | `string` | 否 | `—` | Additional className for the inner `<table>` element. |
| `defaultExpandedKeys` | `Iterable<Key>` | 否 | `—` | Default expanded row keys (uncontrolled). |
| `defaultSelectedKeys` | `Selection` | 否 | `—` | Default selected row keys (uncontrolled). |
| `defaultSortDescriptor` | `SortDescriptor` | 否 | `—` | Default sort descriptor (uncontrolled). |
| `disabledKeys` | `Iterable<string \| number>` | 否 | `—` | Keys of rows that should be disabled. |
| `dragAndDropHooks` | `DragAndDropHooks` | 否 | `—` | Advanced: RAC drag-and-drop hooks for custom DnD scenarios. |
| `expandedKeys` | `Iterable<Key>` | 否 | `—` | Controlled set of expanded row keys. |
| `footer` | `ReactNode` | 否 | `—` | Content rendered into the underlying `Table.Footer` slot, below the table and outside the horizontal scroll area at full root width. Use for pagination, summary rows, or totals. |
| `footerClassName` | `string` | 否 | `—` | Additional className for the footer element (e.g. `justify-between` — the footer is `flex items-center` by default). |
| `getChildren` | `(item: T) => T[]` | 否 | `—` | Returns the child rows for a given item. Providing this enables expandable (tree) rows. |
| `headingHeight` | `number` | 否 | `36` | Header row height in pixels. Required when `virtualized` is true. |
| `isLoadingMore` | `boolean` | 否 | `—` | Whether more data is currently being fetched. |
| `loadMoreContent` | `ReactNode` | 否 | `—` | Content to show inside the load-more sentinel row (e.g. a Spinner). |
| `renderEmptyState` | `() => ReactNode` | 否 | `—` | Render function for the empty state when `data` is empty. |
| `rowHeight` | `number` | 否 | `42` | Fixed row height in pixels. Required when `virtualized` is true. |
| `scrollContainerClassName` | `string` | 否 | `—` | Additional className for the scroll container. |
| `selectedKeys` | `Selection` | 否 | `—` | Controlled selected row keys. |
| `selectionBehavior` | `"replace" \| "toggle"` | 否 | `"toggle"` | Selection interaction model. |
| `selectionMode` | `"none" \| "single" \| "multiple"` | 否 | `"none"` | Row selection mode. |
| `showSelectionCheckboxes` | `boolean` | 否 | `false` | Auto-prepend a checkbox column for selection. |
| `sortDescriptor` | `SortDescriptor` | 否 | `—` | Controlled sort descriptor. When provided, sorting is controlled externally. |
| `treeColumn` | `string` | 否 | `—` | Column id that displays the hierarchy chevron. |
| `treeIndent` | `number` | 否 | `20` | Pixels of inline-start padding added per nested level on the tree column cell. |
| `variant` | `"primary" \| "secondary"` | 否 | `"primary"` | Visual variant passed to the underlying Table. |
| `verticalAlign` | `"bottom" \| "top" \| "middle"` | 否 | `"middle"` | Vertical alignment of cell content within each row. |
| `virtualized` | `boolean` | 否 | `false` | Enable row virtualization for large datasets. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `aria-label` | `string` | 是 | `—` | Accessible label for the table. |
| `onColumnResize` | `(widths: Map<string \| number, ColumnSize>) => void` | 否 | `—` | Callback during column resize. |
| `onColumnResizeEnd` | `(widths: Map<string \| number, ColumnSize>) => void` | 否 | `—` | Callback when resize ends. |
| `onExpandedChange` | `(keys: Set<Key>) => void` | 否 | `—` | Callback fired when the expanded rows change. |
| `onLoadMore` | `() => void` | 否 | `—` | Callback when the load-more sentinel scrolls into view. |
| `onReorder` | `(event: DataGridReorderEvent<T>) => void` | 否 | `—` | Convenience callback for row reorder. |
| `onRowAction` | `(key: string \| number) => void` | 否 | `—` | Callback when a row is actioned (e.g. double-click or Enter). |
| `onSelectionChange` | `(keys: Selection) => void` | 否 | `—` | Callback when selection changes. |
| `onSortChange` | `(descriptor: SortDescriptor) => void` | 否 | `—` | Callback when sort changes. Fires in both controlled and uncontrolled modes. |

</details>

## Token

[`--muted`](/foundations/color) [`--focus`](/foundations/color) [`--ring-offset-width`](/foundations/color) [`--foreground`](/foundations/color) [`--accent`](/foundations/color) [`--surface`](/foundations/color) [`--surface-secondary`](/foundations/color) [`--background`](/foundations/color) [`--separator`](/foundations/color)

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#DataGrid
