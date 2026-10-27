# CellColorPicker

Cube component `CellColorPicker` from `@bosagent/cube-ui/cell-color-picker`.

- 分层：Cube
- 包：`@bosagent/cube-ui/cell-color-picker`
- 状态：建设中

## Import

```tsx
import { CellColorPicker } from "@bosagent/cube-ui/cell-color-picker";
import { CellColorPicker } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `variant` | `"default" \| "secondary"` | 否 | `"default"` | Visual variant. |
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

- `CellColorPicker.Label`
- `CellColorPicker.Popover`
- `CellColorPicker.Swatch`
- `CellColorPicker.Trigger`
- `CellColorPicker.ValueDisplay`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#CellColorPicker
