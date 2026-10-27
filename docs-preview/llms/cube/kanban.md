# Kanban

Cube component `Kanban` from `@bosagent/cube-ui/kanban`.

- 分层：Cube
- 包：`@bosagent/cube-ui/kanban`
- 状态：建设中

## Import

```tsx
import { Kanban } from "@bosagent/cube-ui/kanban";
import { Kanban } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `hideScrollBar` | `boolean` | 否 | `—` | — |
| `isEnabled` | `boolean` | 否 | `true` | Whether scroll shadow detection is enabled |
| `offset` | `number` | 否 | `0` | The scroll offset before showing shadows (in pixels) |
| `orientation` | `"horizontal" \| "vertical"` | 否 | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `"md"` | Size variant controlling card padding, font size, and column width. |
| `variant` | `"fade"` | 否 | `—` | — |
| `visibility` | `ScrollShadowVisibility` | 否 | `"auto"` | Controlled shadow visibility state |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onVisibilityChange` | `(visibility: ScrollShadowVisibility) => void` | 否 | `—` | Callback invoked when shadow visibility changes |

</details>

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

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Kanban
