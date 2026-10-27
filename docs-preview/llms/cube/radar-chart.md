# RadarChart

Cube component `RadarChart` from `@bosagent/cube-ui/radar-chart`.

- 分层：Cube
- 包：`@bosagent/cube-ui/radar-chart`
- 状态：建设中

## Import

```tsx
import { RadarChart } from "@bosagent/cube-ui/radar-chart";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `data` | `Record<string, string \| number>[]` | 是 | `—` | Chart data — array of objects with a category key and numeric series fields. |
| `height` | `number` | 否 | `300` | Chart height in pixels. |
| `width` | `` number \| `${number}%` `` | 否 | `"100%"` | Chart width in pixels or percentage string. |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

## Parts

- `RadarChart.AngleAxis`
- `RadarChart.Grid`
- `RadarChart.Radar`
- `RadarChart.RadiusAxis`
- `RadarChart.Tooltip`
- `RadarChart.TooltipContent`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#RadarChart
