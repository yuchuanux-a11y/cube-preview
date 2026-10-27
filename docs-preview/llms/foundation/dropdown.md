# Dropdown

A dropdown displays a list of actions or options that a user can choose

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Dropdown } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `className` | `string` | 否 | `—` | — |
| `children` | `React.ReactNode` | 是 | `—` | — |
| `defaultOpen` | `boolean` | 否 | `—` | Whether the overlay is open by default (uncontrolled). |
| `isOpen` | `boolean` | 否 | `—` | Whether the overlay is open by default (controlled). |
| `trigger` | `MenuTriggerType` | 否 | `'press'` | How the menu is triggered. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onOpenChange` | `(isOpen: boolean) => void` | 否 | `—` | Handler that is called when the overlay's open state changes. |

</details>

## Parts

- `Dropdown.Item`
- `Dropdown.ItemIndicator`
- `Dropdown.Menu`
- `Dropdown.Popover`
- `Dropdown.Section`
- `Dropdown.SubmenuIndicator`
- `Dropdown.SubmenuTrigger`
- `Dropdown.Trigger`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-70150
