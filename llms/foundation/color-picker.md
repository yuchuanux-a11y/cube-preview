# ColorPicker

A composable color picker that synchronizes color value between multiple color components

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { ColorPicker } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | 是 | `—` | Content of the color picker (Trigger, Popover, etc.) |
| `className` | `string` | 否 | `—` | Additional class name for the wrapper element |
| `defaultValue` | `string \| Color` | 否 | `—` | The default value (uncontrolled). |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `value` | `string \| Color` | 否 | `—` | The current value (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onChange` | `(value: Color) => void` | 否 | `—` | Handler that is called when the value changes. |

</details>

## Parts

- `ColorPicker.Popover`
- `ColorPicker.Trigger`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=18553-86417
