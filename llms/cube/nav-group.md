# NavGroup

Cube component `NavGroup` from `@bosagent/cube-ui/nav-group`.

- 分层：Cube
- 包：`@bosagent/cube-ui/nav-group`
- 状态：建设中

## Import

```tsx
import { NavGroup } from "@bosagent/cube-ui/nav-group";
import { NavGroup } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `label` | `string` | 是 | `—` | Group label, for example a repository name. |
| `action` | `ReactNode` | 否 | `—` | Trailing control shown on hover, focus, and press. Defaults to a “New” plus button. Pass a Dropdown trigger here for the repository menu. |
| `actionLabel` | `string` | 否 | `"New"` | Accessible name for the default plus button. |
| `actionOpen` | `boolean` | 否 | `—` | Keep the trailing action visible, for example while its menu is open. |
| `children` | `ReactNode` | 否 | `—` | Child rows. Rendered in a list when the group is expanded. |
| `defaultExpanded` | `boolean` | 否 | `—` | — |
| `expanded` | `boolean` | 否 | `—` | Expanded shows `folder-open-2` and reveals `children`. There is no selected state. |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onAction` | `() => void` | 否 | `—` | Called by the default plus button. |
| `onExpandedChange` | `(expanded: boolean) => void` | 否 | `—` | — |

</details>

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=23852-1627

## 画廊

[Open in gallery](#NavGroup)
