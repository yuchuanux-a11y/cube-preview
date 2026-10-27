# Stepper

Cube component `Stepper` from `@bosagent/cube-ui/stepper`.

- 分层：Cube
- 包：`@bosagent/cube-ui/stepper`
- 状态：建设中

## Import

```tsx
import { Stepper } from "@bosagent/cube-ui/stepper";
import { Stepper } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | 是 | `—` | — |
| `currentStep` | `number` | 否 | `—` | — |
| `defaultStep` | `number` | 否 | `—` | — |
| `orientation` | `"horizontal" \| "vertical"` | 否 | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onStepChange` | `(step: number) => void` | 否 | `—` | — |

</details>

## Parts

- `Stepper.Content`
- `Stepper.Description`
- `Stepper.Icon`
- `Stepper.Indicator`
- `Stepper.Separator`
- `Stepper.Step`
- `Stepper.Title`
- `Stepper.useStep`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Stepper
