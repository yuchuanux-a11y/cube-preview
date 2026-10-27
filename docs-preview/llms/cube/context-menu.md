# ContextMenu

Cube component `ContextMenu` from `@bosagent/cube-ui/context-menu`.

- 分层：Cube
- 包：`@bosagent/cube-ui/context-menu`
- 状态：建设中

## Import

```tsx
import { ContextMenu } from "@bosagent/cube-ui/context-menu";
import { ContextMenu } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `defaultOpen` | `boolean` | 否 | `—` | Default open state (uncontrolled). |
| `isDisabled` | `boolean` | 否 | `—` | Whether the context menu is disabled. |
| `open` | `boolean` | 否 | `—` | Controlled open state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onOpenChange` | `(open: boolean) => void` | 否 | `—` | Callback when open state changes. |

</details>

## Parts

- `ContextMenu.Item`
- `ContextMenu.ItemIndicator`
- `ContextMenu.Menu`
- `ContextMenu.Popover`
- `ContextMenu.Section`
- `ContextMenu.Separator`
- `ContextMenu.SubmenuIndicator`
- `ContextMenu.SubmenuTrigger`
- `ContextMenu.Trigger`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#ContextMenu
