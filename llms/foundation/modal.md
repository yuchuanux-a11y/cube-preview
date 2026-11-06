# Modal

Dialog overlay for focused user interactions and important content

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Modal } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `state` | `UseOverlayStateReturn` | 否 | `—` | — |
| `children` | `React.ReactNode` | 是 | `—` | — |
| `defaultOpen` | `boolean` | 否 | `—` | Whether the overlay is open by default (uncontrolled). |
| `isOpen` | `boolean` | 否 | `—` | Whether the overlay is open by default (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onOpenChange` | `(isOpen: boolean) => void` | 否 | `—` | Handler that is called when the overlay's open state changes. |

</details>

## Parts

- `Modal.Backdrop`
- `Modal.Body`
- `Modal.CloseTrigger`
- `Modal.Container`
- `Modal.Dialog`
- `Modal.Footer`
- `Modal.Header`
- `Modal.Heading`
- `Modal.Icon`
- `Modal.Trigger`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-77858
