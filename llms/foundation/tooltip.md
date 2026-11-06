# Tooltip

Displays informative text when users hover over or focus on an element

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Tooltip } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `shouldSkipAnimation` | `boolean` | 否 | `false` | Whether to let React Aria skip the enter and exit animations while its global warmup timer is active, i.e. when moving quickly from one tooltip to another. |
| `children` | `React.ReactNode` | 是 | `—` | — |
| `closeDelay` | `number` | 否 | `500` | The delay time for the tooltip to close. [See guidelines](https://spectrum.adobe.com/page/tooltip/#Warmup-and-cooldown). |
| `defaultOpen` | `boolean` | 否 | `—` | Whether the overlay is open by default (uncontrolled). |
| `delay` | `number` | 否 | `1500` | The delay time for the tooltip to show up. [See guidelines](https://spectrum.adobe.com/page/tooltip/#Immediate-or-delayed-appearance). |
| `isDisabled` | `boolean` | 否 | `—` | Whether the tooltip should be disabled, independent from the trigger. |
| `isOpen` | `boolean` | 否 | `—` | Whether the overlay is open by default (controlled). |
| `shouldCloseOnPress` | `boolean` | 否 | `true` | Whether the tooltip should close when the trigger is pressed. |
| `trigger` | `"focus" \| "hover"` | 否 | `'hover'` | By default, opens for both focus and hover. Can be made to open only for focus. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onOpenChange` | `(isOpen: boolean) => void` | 否 | `—` | Handler that is called when the overlay's open state changes. |

</details>

## Parts

- `Tooltip.Arrow`
- `Tooltip.Content`
- `Tooltip.Trigger`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-71565
