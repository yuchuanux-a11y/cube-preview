# NavSectionHeader

Cube component `NavSectionHeader` from `@bosagent/cube-ui/nav-section-header`.

- 分层：Cube
- 包：`@bosagent/cube-ui/nav-section-header`
- 状态：建设中

## Import

```tsx
import { NavSectionHeader } from "@bosagent/cube-ui/nav-section-header";
import { NavSectionHeader } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `label` | `string` | 是 | `—` | — |
| `actions` | `ReactNode` | 否 | `—` | Trailing icon buttons. Kept for `collapsible` as well as `actions`. |
| `children` | `ReactNode` | 否 | `—` | Section body shown while a collapsible header is expanded. |
| `defaultExpanded` | `boolean` | 否 | `—` | — |
| `expanded` | `boolean` | 否 | `—` | Used when `type` is `collapsible`. |
| `type` | `NavSectionHeaderType` | 否 | `—` | `actions` shows trailing buttons, `collapsible` toggles a section, `dateGroup` is a muted label. |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onExpandedChange` | `(expanded: boolean) => void` | 否 | `—` | — |

</details>

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=23867-1380

## 画廊

[Open in gallery](#NavSectionHeader)
