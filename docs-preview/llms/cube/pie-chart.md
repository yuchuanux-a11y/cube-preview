# PieChart

Cube component `PieChart` from `@bosagent/cube-ui/pie-chart`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/pie-chart` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/pie-chart` |

检索：PieChart、pie-chart。

## Import

```tsx
import { PieChart } from "@bosagent/cube-ui/pie-chart";
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
| `height` | `number` | No | `300` | Chart height in pixels. |
| `width` | `` number \| `${number}%` `` | No | `"100%"` | Chart width in pixels or percentage string. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `PieChart.Cell`
- `PieChart.Label`
- `PieChart.Pie`
- `PieChart.Tooltip`
- `PieChart.TooltipContent`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[PieChart](https://yuchuanux-a11y.github.io/cube-preview/#PieChart)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/pie-chart.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import type { ReactNode } from 'react';
import { ChartTooltip } from '@components/chart-tooltip';
import { PieChart } from '@components/pie-chart';
import { Card } from '@heroui/react';

const CHART_COLORS = [
  'var(--chart-4)',
  'var(--chart-3)',
  'var(--chart-2)',
  'var(--chart-1)',
];

const browserData = [
  { name: 'Chrome', value: 62 },
  { name: 'Safari', value: 19 },
  { name: 'Firefox', value: 10 },
  { name: 'Edge', value: 9 },
];

function PieTooltip({
  active,
  payload,
}: {
  active?: boolean;
  payload?: Array<{
    name?: string;
    payload?: { fill?: string };
    value?: number | string;
  }>;
  valueFormatter?: (value: number | string) => ReactNode;
}) {
  const entry = payload?.[0];

  if (!active || !entry) return null;

  return (
    <ChartTooltip>
      <ChartTooltip.Item>
        <ChartTooltip.Indicator color={entry.payload?.fill} />
        <ChartTooltip.Label>{entry.name}</ChartTooltip.Label>
        <ChartTooltip.Value>{entry.value}</ChartTooltip.Value>
      </ChartTooltip.Item>
    </ChartTooltip>
  );
}

export function Default() {
  return (
    <Card className="w-[360px] rounded-2xl">
      <Card.Header>
        <Card.Title className="text-base">Browser Usage</Card.Title>
      </Card.Header>
      <Card.Content className="flex flex-col items-center gap-4">
        <PieChart height={220}>
          <PieChart.Pie
            cx="50%"
            cy="50%"
            data={browserData}
            dataKey="value"
            nameKey="name"
            outerRadius={90}
          >
            {browserData.map((_, idx) => (
              <PieChart.Cell
                key={idx}
                fill={CHART_COLORS[idx % CHART_COLORS.length]}
              />
            ))}
          </PieChart.Pie>
          <PieChart.Tooltip content={<PieTooltip />} />
        </PieChart>
        <div className="flex flex-wrap justify-center gap-x-4 gap-y-1.5">
          {browserData.map((entry, idx) => (
            <div key={entry.name} className="flex items-center gap-1.5">
              <span
                className="size-2.5 rounded-full"
                style={{
                  backgroundColor: CHART_COLORS[idx % CHART_COLORS.length],
                }}
              />
              <span className="text-xs text-muted">{entry.name}</span>
            </div>
          ))}
        </div>
      </Card.Content>
    </Card>
  );
}
```
