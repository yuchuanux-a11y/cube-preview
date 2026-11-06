# NavItem

Cube component `NavItem` from `@bosagent/cube-ui/nav-item`.

- 分层：Cube
- 包：`@bosagent/cube-ui/nav-item`
- 状态：建设中

## Import

```tsx
import { NavItem } from "@bosagent/cube-ui/nav-item";
import { NavItem } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `label` | `string` | 是 | `—` | Row label. Truncates on one line. |
| `actions` | `ReactNode` | 否 | `—` | Icon buttons shown on hover and keyboard focus. They replace `trailing`. The time slot stays. |
| `badge` | `ReactNode` | 否 | `—` | Trailing text badge, for example Early Beta. |
| `href` | `string` | 否 | `—` | Renders the row as a link when set. |
| `icon` | `ReactNode` | 否 | `—` | Leading nav icon. The 12px slot grows to 16px for it. |
| `isDisabled` | `boolean` | 否 | `—` | Disables navigation and hides row actions. Disabled links leave the tab order. |
| `selected` | `boolean` | 否 | `—` | Selected fill, retained during hover/focus. Sets `aria-current="page"`. |
| `shortcut` | `ReactNode` | 否 | `—` | Shortcut such as a Kbd `⌘N`. |
| `status` | `"done" \| "running" \| "needsInput" \| "failed" \| "stopped" \| "prDraft" \| "prOpen" \| "prMerged" \| "prClosed"` | 否 | `—` | Thread status glyph. Ignored while `unread` is set. |
| `time` | `string` | 否 | `—` | Relative time, right-aligned in a 24px tabular slot. Stays visible on hover. |
| `trailing` | `ReactNode` | 否 | `—` | Extra trailing glyph. Hidden while `actions` are showing. |
| `unread` | `boolean` | 否 | `—` | Unread dot. Higher priority than `status`: the 4px accent Badge dot replaces the status glyph. |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onClick` | `(event: MouseEvent<HTMLButtonElement \| HTMLAnchorElement>) => void` | 否 | `—` | — |

</details>

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=23852-1546

## 画廊

[Open in gallery](#NavItem)
