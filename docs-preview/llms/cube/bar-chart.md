# BarChart

Cube component `BarChart` from `@bosagent/cube-ui/bar-chart`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/bar-chart` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/bar-chart` |

检索：BarChart、bar-chart。

## Import

```tsx
import { BarChart } from "@bosagent/cube-ui/bar-chart";
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
| `layout` | `"horizontal" \| "vertical"` | No | `"horizontal"` | Bar layout direction. Use "vertical" for horizontal bar charts. |
| `margin` | `{ bottom?: number; left?: number; right?: number; top?: number; }` | No | `{ top: 8, right: 8, bottom: 0, left: 0 }` | Recharts margin. |
| `width` | `` number \| `${number}%` `` | No | `"100%"` | Chart width in pixels or percentage string like "100%". |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `BarChart.Bar`
- `BarChart.Grid`
- `BarChart.Tooltip`
- `BarChart.TooltipContent`
- `BarChart.XAxis`
- `BarChart.YAxis`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[BarChart](https://yuchuanux-a11y.github.io/cube-preview/#BarChart)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/bar-chart.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { BarChart } from '@components/bar-chart';
import { ChartTooltip } from '@components/chart-tooltip';
import { Card } from '@heroui/react';

const revenueByChannel = [
  { direct: 3200, month: 'Jan', online: 4200, retail: 2800 },
  { direct: 4100, month: 'Feb', online: 5800, retail: 3400 },
  { direct: 3800, month: 'Mar', online: 4900, retail: 3100 },
  { direct: 5200, month: 'Apr', online: 7200, retail: 4200 },
  { direct: 4600, month: 'May', online: 6100, retail: 3800 },
  { direct: 5800, month: 'Jun', online: 8400, retail: 4500 },
];

export function Default() {
  return (
    <Card className="w-full max-w-[480px] rounded-2xl">
      <Card.Header>
        <Card.Title className="text-base">Revenue by Channel</Card.Title>
      </Card.Header>
      <Card.Content>
        <BarChart data={revenueByChannel} height={220}>
          <BarChart.Grid vertical={false} />
          <BarChart.XAxis dataKey="month" tickMargin={8} />
          <BarChart.YAxis
            tickFormatter={(v: number) => `$${(v / 1000).toFixed(0)}k`}
            width={40}
          />
          <BarChart.Bar
            barSize={10}
            dataKey="online"
            fill="var(--chart-3)"
            name="Online"
            radius={[4, 4, 0, 0]}
          />
          <BarChart.Bar
            barSize={10}
            dataKey="retail"
            fill="var(--chart-2)"
            name="Retail"
            radius={[4, 4, 0, 0]}
          />
          <BarChart.Bar
            barSize={10}
            dataKey="direct"
            fill="var(--chart-1)"
            name="Direct"
            radius={[4, 4, 0, 0]}
          />
          <BarChart.Tooltip
            content={({ active, label, payload }) => {
              if (
                !active ||
                !payload?.length ||
                !payload.every((entry) => typeof entry.value === 'number')
              )
                return null;

              const total = payload.reduce(
                (sum, entry) => sum + ((entry.value as number) ?? 0),
                0
              );

              return (
                <ChartTooltip>
                  <ChartTooltip.Header>{label}</ChartTooltip.Header>
                  {payload.map((entry, idx) => (
                    <ChartTooltip.Item key={idx}>
                      <ChartTooltip.Indicator color={entry.fill} />
                      <ChartTooltip.Label>{entry.name}</ChartTooltip.Label>
                      <ChartTooltip.Value>
                        ${Number(entry.value).toLocaleString()}
                      </ChartTooltip.Value>
                    </ChartTooltip.Item>
                  ))}
                  <div className="mt-1 flex items-center justify-between border-t border-separator pt-1.5">
                    <span className="text-xs font-medium text-muted">
                      Total
                    </span>
                    <span className="text-xs font-semibold text-foreground">
                      ${total.toLocaleString()}
                    </span>
                  </div>
                </ChartTooltip>
              );
            }}
          />
        </BarChart>
      </Card.Content>
    </Card>
  );
}
```
