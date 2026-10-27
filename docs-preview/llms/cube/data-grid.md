# DataGrid

Cube component `DataGrid` from `@bosagent/cube-ui/data-grid`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/data-grid` |
| 分层 | Cube |
| 成熟度 | 代码可预览（@bosagent/cube-ui/data-grid）。设计 registry 没有 DataGrid 规范条目。适用边界建设中。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/data-grid` |

检索：DataGrid、data-grid。

## Import

```tsx
import { DataGrid } from "@bosagent/cube-ui/data-grid";
import { DataGrid } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## 适用

建设中。设计 registry 没有这条用法。

## 不适用

建设中。

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `aria-label` | `string` | Yes | `—` | Accessible label for the table. |
| `columns` | `DataGridColumn<T>[]` | Yes | `—` | Column definitions. |
| `data` | `T[]` | Yes | `—` | Row data array. |
| `getRowId` | `(item: T) => string \| number` | Yes | `—` | Extracts a unique key from each row item. |
| `allowsColumnResize` | `boolean` | No | `false` | Enable column resizing on columns that opt in. |
| `className` | `string` | No | `—` | Additional className for the root wrapper. |
| `contentClassName` | `string` | No | `—` | Additional className for the inner `<table>` element. |
| `defaultExpandedKeys` | `Iterable<Key>` | No | `—` | Default expanded row keys (uncontrolled). |
| `defaultSelectedKeys` | `Selection` | No | `—` | Default selected row keys (uncontrolled). |
| `defaultSortDescriptor` | `SortDescriptor` | No | `—` | Default sort descriptor (uncontrolled). |
| `disabledKeys` | `Iterable<string \| number>` | No | `—` | Keys of rows that should be disabled. |
| `dragAndDropHooks` | `DragAndDropHooks` | No | `—` | Advanced: RAC drag-and-drop hooks for custom DnD scenarios. |
| `expandedKeys` | `Iterable<Key>` | No | `—` | Controlled set of expanded row keys. |
| `footer` | `ReactNode` | No | `—` | Content rendered into the underlying `Table.Footer` slot, below the table and outside the horizontal scroll area at full root width. Use for pagination, summary rows, or totals. |
| `footerClassName` | `string` | No | `—` | Additional className for the footer element (e.g. `justify-between` — the footer is `flex items-center` by default). |
| `getChildren` | `(item: T) => T[]` | No | `—` | Returns the child rows for a given item. Providing this enables expandable (tree) rows. |
| `headingHeight` | `number` | No | `36` | Header row height in pixels. Required when `virtualized` is true. |
| `isLoadingMore` | `boolean` | No | `—` | Whether more data is currently being fetched. |
| `loadMoreContent` | `ReactNode` | No | `—` | Content to show inside the load-more sentinel row (e.g. a Spinner). |
| `onColumnResize` | `(widths: Map<string \| number, ColumnSize>) => void` | No | `—` | Callback during column resize. |
| `onColumnResizeEnd` | `(widths: Map<string \| number, ColumnSize>) => void` | No | `—` | Callback when resize ends. |
| `onExpandedChange` | `(keys: Set<Key>) => void` | No | `—` | Callback fired when the expanded rows change. |
| `onLoadMore` | `() => void` | No | `—` | Callback when the load-more sentinel scrolls into view. |
| `onReorder` | `(event: DataGridReorderEvent<T>) => void` | No | `—` | Convenience callback for row reorder. |
| `onRowAction` | `(key: string \| number) => void` | No | `—` | Callback when a row is actioned (e.g. double-click or Enter). |
| `onSelectionChange` | `(keys: Selection) => void` | No | `—` | Callback when selection changes. |
| `onSortChange` | `(descriptor: SortDescriptor) => void` | No | `—` | Callback when sort changes. Fires in both controlled and uncontrolled modes. |
| `renderEmptyState` | `() => ReactNode` | No | `—` | Render function for the empty state when `data` is empty. |
| `rowHeight` | `number` | No | `42` | Fixed row height in pixels. Required when `virtualized` is true. |
| `scrollContainerClassName` | `string` | No | `—` | Additional className for the scroll container. |
| `selectedKeys` | `Selection` | No | `—` | Controlled selected row keys. |
| `selectionBehavior` | `"replace" \| "toggle"` | No | `"toggle"` | Selection interaction model. |
| `selectionMode` | `"none" \| "single" \| "multiple"` | No | `"none"` | Row selection mode. |
| `showSelectionCheckboxes` | `boolean` | No | `false` | Auto-prepend a checkbox column for selection. |
| `sortDescriptor` | `SortDescriptor` | No | `—` | Controlled sort descriptor. When provided, sorting is controlled externally. |
| `treeColumn` | `string` | No | `—` | Column id that displays the hierarchy chevron. |
| `treeIndent` | `number` | No | `20` | Pixels of inline-start padding added per nested level on the tree column cell. |
| `variant` | `"primary" \| "secondary"` | No | `"primary"` | Visual variant passed to the underlying Table. |
| `verticalAlign` | `"bottom" \| "top" \| "middle"` | No | `"middle"` | Vertical alignment of cell content within each row. |
| `virtualized` | `boolean` | No | `false` | Enable row virtualization for large datasets. |

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

- [`--muted`](/foundations/theme)
- [`--focus`](/foundations/theme)
- [`--ring-offset-width`](/foundations/theme)
- [`--foreground`](/foundations/theme)
- [`--accent`](/foundations/theme)
- [`--surface`](/foundations/theme)
- [`--surface-secondary`](/foundations/theme)
- [`--background`](/foundations/theme)
- [`--separator`](/foundations/theme)

从 packages/cube-ui/src/css/components/data-grid.css 的 var() 引用抽出，且这些名字在 cube-contract.css 里存在。同文件还有 --color-surface 等 Tailwind 颜色映射，不是 cube-contract.css 里的变量。未做逐项视觉验收。

## 画廊

[DataGrid](https://yuchuanux-a11y.github.io/cube-preview/#DataGrid)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/data-grid.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { useState } from 'react';
import type { Selection } from 'react-aria-components/GridList';
import { DataGrid, type DataGridColumn } from '@components/data-grid';
import {
  CircleFill,
  Copy,
  EllipsisVertical,
  Eye,
  Pencil,
  TrashBin,
} from '@gravity-ui/icons';
import { Button, Chip, Dropdown, Label } from '@heroui/react';

interface Payment {
  id: string;
  customer: string;
  email: string;
  amount: number;
  fee: number;
  net: number;
  status: 'succeeded' | 'processing' | 'failed' | 'refunded';
  method: string;
  region: string;
  description: string;
  date: string;
}

const payments: Payment[] = [
  {
    amount: 1999.0,
    customer: 'Olivia Martin',
    date: '2025-12-01',
    description: 'Annual subscription — Pro plan',
    email: 'olivia@example.com',
    fee: 59.97,
    id: 'pay_1N3x7K',
    method: 'Visa •••• 4242',
    net: 1939.03,
    region: 'North America',
    status: 'succeeded',
  },
  {
    amount: 39.0,
    customer: 'Jackson Lee',
    date: '2025-12-02',
    description: 'Monthly add-on — Extra seats',
    email: 'jackson@example.com',
    fee: 1.43,
    id: 'pay_1N3x8L',
    method: 'Mastercard •••• 5555',
    net: 37.57,
    region: 'North America',
    status: 'processing',
  },
  {
    amount: 299.0,
    customer: 'Isabella Nguyen',
    date: '2025-12-03',
    description: 'Quarterly subscription — Team plan',
    email: 'isabella@example.com',
    fee: 8.97,
    id: 'pay_1N3x9M',
    method: 'Visa •••• 1234',
    net: 290.03,
    region: 'Asia Pacific',
    status: 'succeeded',
  },
  {
    amount: 99.0,
    customer: 'William Kim',
    date: '2025-12-04',
    description: 'Monthly subscription — Starter plan',
    email: 'will@example.com',
    fee: 3.17,
    id: 'pay_1N3xAN',
    method: 'Amex •••• 3782',
    net: 95.83,
    region: 'Asia Pacific',
    status: 'failed',
  },
  {
    amount: 450.0,
    customer: 'Sofia Davis',
    date: '2025-12-05',
    description: 'One-time purchase — Enterprise setup',
    email: 'sofia@example.com',
    fee: 13.5,
    id: 'pay_1N3xBP',
    method: 'Visa •••• 9012',
    net: 436.5,
    region: 'Europe',
    status: 'succeeded',
  },
  {
    amount: 150.0,
    customer: 'Liam Johnson',
    date: '2025-12-06',
    description: 'Monthly subscription — Pro plan',
    email: 'liam@example.com',
    fee: 4.5,
    id: 'pay_1N3xCQ',
    method: 'Mastercard •••• 6789',
    net: 145.5,
    region: 'Europe',
    status: 'refunded',
  },
  {
    amount: 2450.0,
    customer: 'Emma Wilson',
    date: '2025-12-07',
    description: 'Annual subscription — Enterprise plan',
    email: 'emma@example.com',
    fee: 73.5,
    id: 'pay_1N3xDR',
    method: 'Visa •••• 4242',
    net: 2376.5,
    region: 'North America',
    status: 'succeeded',
  },
];

const statusColorMap: Record<
  Payment['status'],
  'success' | 'warning' | 'danger' | 'default'
> = {
  failed: 'danger',
  processing: 'warning',
  refunded: 'default',
  succeeded: 'success',
};

function formatCurrency(amount: number) {
  return new Intl.NumberFormat('en-US', {
    currency: 'USD',
    style: 'currency',
  }).format(amount);
}

function formatDate(dateStr: string) {
  return new Date(dateStr).toLocaleDateString('en-US', {
    day: 'numeric',
    month: 'short',
    year: 'numeric',
  });
}

function RowActionsMenu({ paymentId }: { paymentId: string }) {
  return (
    <Dropdown>
      <Button isIconOnly aria-label="Row actions" size="sm" variant="tertiary">
        <EllipsisVertical />
      </Button>
      <Dropdown.Popover className="min-w-[180px]">
        <Dropdown.Menu
          onAction={(key) => {
            if (key === 'copy') {
              navigator.clipboard.writeText(paymentId);
            }
          }}
        >
          <Dropdown.Item id="copy" textValue="Copy payment ID">
            <Copy />
            <Label>Copy payment ID</Label>
          </Dropdown.Item>
          <Dropdown.Item id="view" textValue="View details">
            <Eye />
            <Label>View details</Label>
          </Dropdown.Item>
          <Dropdown.Item id="edit" textValue="Edit payment">
            <Pencil />
            <Label>Edit payment</Label>
          </Dropdown.Item>
          <Dropdown.Item id="delete" textValue="Delete" variant="danger">
            <TrashBin className="text-danger" />
            <Label>Delete</Label>
          </Dropdown.Item>
        </Dropdown.Menu>
      </Dropdown.Popover>
    </Dropdown>
  );
}

export function Default() {
  const [selectedKeys, setSelectedKeys] = useState<Selection>(() => new Set());

  const columns: DataGridColumn<Payment>[] = [
    {
      accessorKey: 'customer',
      allowsResizing: true,
      allowsSorting: true,
      cell: (item) => (
        <div className="flex flex-col">
          <span className="text-sm font-medium">{item.customer}</span>
          <span className="text-xs text-muted">{item.email}</span>
        </div>
      ),
      header: 'Customer',
      id: 'customer',
      isRowHeader: true,
      minWidth: 200,
    },
    {
      accessorKey: 'id',
      allowsResizing: true,
      cellClassName: 'font-mono text-xs text-muted',
      header: 'Transaction ID',
      id: 'id',
      minWidth: 130,
    },
    {
      accessorKey: 'status',
      allowsResizing: true,
      allowsSorting: true,
      cell: (item) => (
        <Chip color={statusColorMap[item.status]} size="sm" variant="soft">
          <CircleFill width={6} />
          <Chip.Label className="capitalize">{item.status}</Chip.Label>
        </Chip>
      ),
      header: 'Status',
      id: 'status',
      minWidth: 120,
    },
    {
      accessorKey: 'amount',
      align: 'end',
      allowsResizing: true,
      allowsSorting: true,
      cell: (item) => (
        <span className="font-medium tabular-nums">
          {formatCurrency(item.amount)}
        </span>
      ),
      header: 'Amount',
      id: 'amount',
      minWidth: 110,
    },
    {
      accessorKey: 'fee',
      align: 'end',
      allowsResizing: true,
      allowsSorting: true,
      cell: (item) => (
        <span className="text-muted tabular-nums">
          {formatCurrency(item.fee)}
        </span>
      ),
      header: 'Fee',
      id: 'fee',
      minWidth: 90,
    },
    {
      accessorKey: 'net',
      align: 'end',
      allowsResizing: true,
      allowsSorting: true,
      cell: (item) => (
        <span className="font-medium tabular-nums">
          {formatCurrency(item.net)}
        </span>
      ),
      header: 'Net',
      id: 'net',
      minWidth: 110,
    },
    {
      accessorKey: 'method',
      allowsResizing: true,
      header: 'Payment Method',
      id: 'method',
      minWidth: 170,
    },
    {
      accessorKey: 'region',
      allowsResizing: true,
      allowsSorting: true,
      header: 'Region',
      id: 'region',
      minWidth: 130,
    },
    {
      accessorKey: 'description',
      allowsResizing: true,
      cellClassName: 'text-muted',
      header: 'Description',
      id: 'description',
      minWidth: 240,
    },
    {
      accessorKey: 'date',
      allowsResizing: true,
      allowsSorting: true,
      cell: (item) => (
        <span className="text-muted tabular-nums">{formatDate(item.date)}</span>
      ),
      header: 'Date',
      id: 'date',
      minWidth: 120,
    },
    {
      align: 'end',
      allowsResizing: false,
      cell: (item) => <RowActionsMenu paymentId={item.id} />,
      header: '',
      id: 'actions',
      pinned: 'end',
      width: 50,
    },
  ];

  const selectionCount =
    selectedKeys === 'all'
      ? payments.length
      : (selectedKeys as Set<string>).size;

  return (
    <div className="flex w-full max-w-5xl flex-col gap-3">
      <DataGrid
        allowsColumnResize
        showSelectionCheckboxes
        aria-label="Payments"
        columns={columns}
        contentClassName="min-w-[1400px]"
        data={payments}
        defaultSortDescriptor={{ column: 'customer', direction: 'ascending' }}
        getRowId={(item) => item.id}
        renderEmptyState={() => 'No payments found.'}
        selectedKeys={selectedKeys}
        selectionMode="multiple"
        footer={
          <span className="text-sm text-muted">
            {selectionCount > 0
              ? `${selectionCount} of ${payments.length} row(s) selected`
              : `${payments.length} payments`}
          </span>
        }
        footerClassName="justify-end"
        variant="primary"
        onSelectionChange={setSelectedKeys}
      />
    </div>
  );
}
```
