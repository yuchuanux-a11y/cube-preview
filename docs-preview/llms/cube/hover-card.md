# HoverCard

Cube component `HoverCard` from `@bosagent/cube-ui/hover-card`.

- 分层：Cube
- 包：`@bosagent/cube-ui/hover-card`
- 状态：建设中

## Import

```tsx
import { HoverCard } from "@bosagent/cube-ui/hover-card";
import { HoverCard } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `closeDelay` | `number` | 否 | `300` | Time in ms before the hover card closes after pointer/focus leave. |
| `defaultOpen` | `boolean` | 否 | `—` | Default open state (uncontrolled). |
| `isDisabled` | `boolean` | 否 | `—` | Whether the hover card is disabled and never opens. |
| `open` | `boolean` | 否 | `—` | Controlled open state. |
| `openDelay` | `number` | 否 | `700` | Time in ms before the hover card opens after hover. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onOpenChange` | `(open: boolean) => void` | 否 | `—` | Callback when open state changes. |

</details>

## Parts

- `HoverCard.Arrow`
- `HoverCard.Content`
- `HoverCard.Trigger`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#HoverCard
