# ComposedChart

Cube component `ComposedChart` from `@bosagent/cube-ui/composed-chart`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/composed-chart` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/composed-chart` |

检索：ComposedChart、composed-chart。

## Import

```tsx
import { ComposedChart } from "@bosagent/cube-ui/composed-chart";
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

- `ComposedChart.Area`
- `ComposedChart.Bar`
- `ComposedChart.Grid`
- `ComposedChart.Line`
- `ComposedChart.Tooltip`
- `ComposedChart.TooltipContent`
- `ComposedChart.XAxis`
- `ComposedChart.YAxis`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ComposedChart](https://yuchuanux-a11y.github.io/cube-preview/#ComposedChart)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/composed-chart.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { ChartTooltip } from '@components/chart-tooltip';
import { ComposedChart } from '@components/composed-chart';
import { Card } from '@heroui/react';

const data = [
  { month: 'Jan', orders: 320, revenue: 4200 },
  { month: 'Feb', orders: 450, revenue: 5800 },
  { month: 'Mar', orders: 380, revenue: 4900 },
  { month: 'Apr', orders: 520, revenue: 7200 },
  { month: 'May', orders: 480, revenue: 6100 },
  { month: 'Jun', orders: 600, revenue: 8400 },
  { month: 'Jul', orders: 550, revenue: 7800 },
  { month: 'Aug', orders: 680, revenue: 9200 },
  { month: 'Sep', orders: 620, revenue: 8600 },
  { month: 'Oct', orders: 750, revenue: 10200 },
  { month: 'Nov', orders: 700, revenue: 9800 },
  { month: 'Dec', orders: 820, revenue: 11500 },
];

export function Default() {
  return (
    <Card className="w-full rounded-2xl">
      <Card.Header>
        <Card.Title className="text-base">Revenue & Orders</Card.Title>
        <div className="flex items-center gap-3">
          <div className="flex items-center gap-1.5">
            <span
              className="size-3 rounded-full"
              style={{ backgroundColor: 'var(--chart-3)' }}
            />
            <span className="text-xs text-muted">Revenue</span>
          </div>
          <div className="flex items-center gap-1.5">
            <span
              className="size-3 rounded-full"
              style={{ backgroundColor: 'var(--chart-1)' }}
            />
            <span className="text-xs text-muted">Orders</span>
          </div>
        </div>
      </Card.Header>
      <Card.Content>
        <ComposedChart data={data} height={260}>
          <ComposedChart.Grid vertical={false} />
          <ComposedChart.XAxis dataKey="month" tickMargin={8} />
          <ComposedChart.YAxis
            tickFormatter={(v: number) => `$${(v / 1000).toFixed(0)}k`}
            width={40}
            yAxisId="left"
          />
          <ComposedChart.YAxis orientation="right" width={40} yAxisId="right" />
          <ComposedChart.Bar
            barSize={16}
            dataKey="revenue"
            fill="var(--chart-3)"
            name="Revenue"
            radius={[4, 4, 0, 0]}
            yAxisId="left"
          />
          <ComposedChart.Line
            dataKey="orders"
            dot={false}
            name="Orders"
            stroke="var(--chart-1)"
            strokeWidth={2}
            type="monotone"
            yAxisId="right"
          />
          <ComposedChart.Tooltip
            content={({ active, label, payload }) => {
              if (!active || !payload?.length) return null;

              return (
                <ChartTooltip>
                  <ChartTooltip.Header>{label}</ChartTooltip.Header>
                  {payload.map((entry) => {
                    const isRevenue = entry.dataKey === 'revenue';

                    return (
                      <ChartTooltip.Item key={String(entry.dataKey)}>
                        <ChartTooltip.Indicator
                          color={entry.color ?? entry.fill ?? entry.stroke}
                        />
                        <ChartTooltip.Label>{entry.name}</ChartTooltip.Label>
                        <ChartTooltip.Value>
                          {isRevenue
                            ? `$${Number(entry.value).toLocaleString()}`
                            : Number(entry.value).toLocaleString()}
                        </ChartTooltip.Value>
                      </ChartTooltip.Item>
                    );
                  })}
                </ChartTooltip>
              );
            }}
          />
        </ComposedChart>
      </Card.Content>
    </Card>
  );
}
```
