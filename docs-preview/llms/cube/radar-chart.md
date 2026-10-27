# RadarChart

Cube component `RadarChart` from `@bosagent/cube-ui/radar-chart`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/radar-chart` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/radar-chart` |

检索：RadarChart、radar-chart。

## Import

```tsx
import { RadarChart } from "@bosagent/cube-ui/radar-chart";
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
| `data` | `Record<string, string \| number>[]` | Yes | `—` | Chart data — array of objects with a category key and numeric series fields. |
| `height` | `number` | No | `300` | Chart height in pixels. |
| `width` | `` number \| `${number}%` `` | No | `"100%"` | Chart width in pixels or percentage string. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `RadarChart.AngleAxis`
- `RadarChart.Grid`
- `RadarChart.Radar`
- `RadarChart.RadiusAxis`
- `RadarChart.Tooltip`
- `RadarChart.TooltipContent`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[RadarChart](https://yuchuanux-a11y.github.io/cube-preview/#RadarChart)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/radar-chart.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { ChartTooltip } from '@components/chart-tooltip';
import { RadarChart } from '@components/radar-chart';
import { Card } from '@heroui/react';

const skillsData = [
  { category: 'Design', score: 86 },
  { category: 'Frontend', score: 92 },
  { category: 'Backend', score: 74 },
  { category: 'DevOps', score: 65 },
  { category: 'Testing', score: 78 },
  { category: 'Leadership', score: 70 },
];

export function Default() {
  return (
    <Card className="w-[420px] rounded-2xl">
      <Card.Header>
        <Card.Title className="text-base">Skill Assessment</Card.Title>
      </Card.Header>
      <Card.Content className="flex flex-col items-center">
        <RadarChart data={skillsData} height={280}>
          <RadarChart.Grid />
          <RadarChart.AngleAxis dataKey="category" />
          <RadarChart.Radar
            dataKey="score"
            dot={{ fill: 'var(--chart-3)', r: 3, strokeWidth: 0 }}
            fill="var(--chart-3)"
            fillOpacity={0.15}
            name="Score"
            stroke="var(--chart-3)"
            strokeWidth={2}
          />
          <RadarChart.Tooltip
            content={({ active, payload }) => {
              if (!active || !payload?.length) return null;
              const category = payload[0]?.payload?.category as
                | string
                | undefined;

              return (
                <ChartTooltip>
                  {category ? (
                    <ChartTooltip.Header>{category}</ChartTooltip.Header>
                  ) : null}
                  {payload.map((entry) => (
                    <ChartTooltip.Item key={String(entry.dataKey)}>
                      <ChartTooltip.Indicator
                        color={entry.color ?? entry.stroke ?? entry.fill}
                      />
                      <ChartTooltip.Label>{entry.name}</ChartTooltip.Label>
                      <ChartTooltip.Value>{entry.value}</ChartTooltip.Value>
                    </ChartTooltip.Item>
                  ))}
                </ChartTooltip>
              );
            }}
          />
        </RadarChart>
      </Card.Content>
    </Card>
  );
}
```
