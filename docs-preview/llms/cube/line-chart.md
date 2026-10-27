# LineChart

Cube component `LineChart` from `@bosagent/cube-ui/line-chart`.

- 分层：Cube
- 包：`@bosagent/cube-ui/line-chart`
- 状态：建设中

## Import

```tsx
import { LineChart } from "@bosagent/cube-ui/line-chart";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `data` | `Record<string, string \| number>[]` | 是 | `—` | Chart data — array of objects with numeric/string fields for each series. |
| `height` | `number` | 否 | `300` | Chart height in pixels. |
| `margin` | `{ bottom?: number; left?: number; right?: number; top?: number; }` | 否 | `{ top: 8, right: 8, bottom: 0, left: 0 }` | Recharts margin. |
| `width` | `` number \| `${number}%` `` | 否 | `"100%"` | Chart width in pixels or percentage string like "100%". |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

## Parts

- `LineChart.Grid`
- `LineChart.Line`
- `LineChart.Tooltip`
- `LineChart.TooltipContent`
- `LineChart.XAxis`
- `LineChart.YAxis`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#LineChart
