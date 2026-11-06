# ApprovalCard

Cube component `ApprovalCard` from `@bosagent/cube-ui/approval-card`.

- 分层：Cube
- 包：`@bosagent/cube-ui/approval-card`
- 状态：建设中

## Import

```tsx
import { ApprovalCard } from "@bosagent/cube-ui/approval-card";
import { ApprovalCard } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `question` | `string` | 是 | `—` | — |
| `confirmation` | `string` | 否 | `—` | — |
| `confirmLabel` | `string` | 否 | `—` | — |
| `context` | `string` | 否 | `—` | — |
| `customLabel` | `string` | 否 | `—` | — |
| `customPlaceholder` | `string` | 否 | `—` | — |
| `customValue` | `string` | 否 | `—` | — |
| `error` | `string` | 否 | `—` | — |
| `mode` | `ApprovalMode` | 否 | `—` | — |
| `options` | `readonly ApprovalOption[]` | 否 | `—` | — |
| `showCustom` | `boolean` | 否 | `—` | — |
| `state` | `ApprovalStatus` | 否 | `—` | — |
| `step` | `ApprovalStep` | 否 | `—` | — |
| `summary` | `string` | 否 | `—` | — |
| `value` | `string \| readonly string[]` | 否 | `—` | Selected option id, or ids when `mode` is `multiple`. |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onConfirm` | `() => void` | 否 | `—` | — |
| `onCustomValueChange` | `(value: string) => void` | 否 | `—` | — |
| `onDismiss` | `() => void` | 否 | `—` | — |
| `onRetry` | `() => void` | 否 | `—` | — |
| `onReview` | `() => void` | 否 | `—` | — |
| `onStepChange` | `(index: number) => void` | 否 | `—` | — |
| `onValueChange` | `(value: string \| readonly string[]) => void` | 否 | `—` | — |

</details>

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=24028-3587

## 画廊

[Open in gallery](#ApprovalCard)
