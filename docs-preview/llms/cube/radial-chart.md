# RadialChart

Cube component `RadialChart` from `@bosagent/cube-ui/radial-chart`.

- 分层：Cube
- 包：`@bosagent/cube-ui/radial-chart`
- 状态：建设中

## Import

```tsx
import { RadialChart } from "@bosagent/cube-ui/radial-chart";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `data` | `Record<string, string \| number>[]` | 是 | `—` | Chart data — array of objects. Each entry becomes a concentric ring. |
| `barSize` | `number` | 否 | `10` | Bar thickness in pixels. |
| `endAngle` | `number` | 否 | `-270` | End angle in degrees. |
| `height` | `number` | 否 | `300` | Chart height in pixels. |
| `innerRadius` | `string \| number` | 否 | `"30%"` | Inner radius of the bar area. |
| `outerRadius` | `string \| number` | 否 | `"80%"` | Outer radius of the bar area. |
| `startAngle` | `number` | 否 | `90` | Start angle in degrees. |
| `width` | `` number \| `${number}%` `` | 否 | `"100%"` | Chart width in pixels or percentage string. |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

## Parts

- `RadialChart.AngleAxis`
- `RadialChart.Bar`
- `RadialChart.Cell`
- `RadialChart.Tooltip`
- `RadialChart.TooltipContent`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#RadialChart
