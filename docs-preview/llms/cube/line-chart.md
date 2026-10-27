# LineChart

Cube component `LineChart` from `@bosagent/cube-ui/line-chart`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/line-chart` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/line-chart` |

检索：LineChart、line-chart。

## Import

```tsx
import { LineChart } from "@bosagent/cube-ui/line-chart";
```

## Preview

The docs page renders a live preview of the real component.

## 适用

建设中。设计 registry 没有这条用法。

## 不适用

建设中。

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `data` | `Record<string, string \| number>[]` | Yes | `—` | Chart data — array of objects with numeric/string fields for each series. |
| `height` | `number` | No | `300` | Chart height in pixels. |
| `margin` | `{ bottom?: number; left?: number; right?: number; top?: number; }` | No | `{ top: 8, right: 8, bottom: 0, left: 0 }` | Recharts margin. |
| `width` | `` number \| `${number}%` `` | No | `"100%"` | Chart width in pixels or percentage string like "100%". |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `LineChart.Grid`
- `LineChart.Line`
- `LineChart.Tooltip`
- `LineChart.TooltipContent`
- `LineChart.XAxis`
- `LineChart.YAxis`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[LineChart](https://yuchuanux-a11y.github.io/cube-preview/#LineChart)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/line-chart.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
import { LineChart } from '@components/line-chart';

const chartData = [
  { month: 'Jan', revenue: 42 },
  { month: 'Feb', revenue: 58 },
  { month: 'Mar', revenue: 51 },
  { month: 'Apr', revenue: 74 },
  { month: 'May', revenue: 69 },
  { month: 'Jun', revenue: 92 },
];

export function Default() {
  return (
    <div className="w-full max-w-[520px] min-w-[280px] rounded-lg border border-neutral-200 bg-white p-4">
      <LineChart data={chartData} height={180}>
        <LineChart.Grid strokeDasharray="3 3" vertical={false} />
        <LineChart.XAxis dataKey="month" tickLine={false} />
        <LineChart.YAxis tickLine={false} />
        <LineChart.Tooltip content={<LineChart.TooltipContent />} />
        <LineChart.Line
          dataKey="revenue"
          name="Revenue"
          stroke="#2563eb"
          strokeWidth={2}
          type="monotone"
        />
      </LineChart>
    </div>
  );
}
```
