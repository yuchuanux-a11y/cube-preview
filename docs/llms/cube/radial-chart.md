# RadialChart

Cube component `RadialChart` from `@bosagent/cube-ui/radial-chart`.

Cube component. Source: `packages/cube-ui/src/components/radial-chart`.

## Import

```tsx
import { RadialChart } from "@bosagent/cube-ui/radial-chart";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `data` | `Record<string, string \| number>[]` | Yes | `—` | Chart data — array of objects. Each entry becomes a concentric ring. |
| `barSize` | `number` | No | `10` | Bar thickness in pixels. |
| `endAngle` | `number` | No | `-270` | End angle in degrees. |
| `height` | `number` | No | `300` | Chart height in pixels. |
| `innerRadius` | `string \| number` | No | `"30%"` | Inner radius of the bar area. |
| `outerRadius` | `string \| number` | No | `"80%"` | Outer radius of the bar area. |
| `startAngle` | `number` | No | `90` | Start angle in degrees. |
| `width` | `` number \| `${number}%` `` | No | `"100%"` | Chart width in pixels or percentage string. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `RadialChart.AngleAxis`
- `RadialChart.Bar`
- `RadialChart.Cell`
- `RadialChart.Tooltip`
- `RadialChart.TooltipContent`

## Example source

```tsx
'use client';

import type { ReactNode } from 'react';
import { ChartTooltip } from '@components/chart-tooltip';
import { RadialChart } from '@components/radial-chart';
import { Card } from '@heroui/react';

const energyData = [
  {
    fill: 'var(--chart-4)',
    name: 'Calories',
    value: 200,
    valueText: '1,623/2,000 kcal',
  },
  {
    fill: 'var(--chart-3)',
    name: 'Steps',
    value: 350,
    valueText: '8,328/10,000 steps',
  },
  {
    fill: 'var(--chart-2)',
    name: 'Exercise',
    value: 250,
    valueText: '25/120 min',
  },
];

function RadialTooltip({
  payload,
  valueFormatter,
}: {
  active?: boolean;
  payload?: Array<{
    name?: string;
    payload?: Record<string, unknown>;
    value?: number | string;
  }>;
  valueFormatter?: (value: number | string) => ReactNode;
}) {
  const entry = payload?.[0];

  if (!entry?.payload) return null;

  const name = (entry.payload['name'] as string) ?? entry.name;
  const value = (entry.payload['value'] as number) ?? entry.value;
  const fill = entry.payload['fill'] as string;

  return (
    <ChartTooltip>
      <ChartTooltip.Item>
        <ChartTooltip.Indicator color={fill} />
        <ChartTooltip.Label>{name}</ChartTooltip.Label>
        <ChartTooltip.Value>
          {valueFormatter && value != null ? valueFormatter(value) : value}
        </ChartTooltip.Value>
      </ChartTooltip.Item>
    </ChartTooltip>
  );
}

export function Default() {
  return (
    <Card className="w-[380px] rounded-2xl">
      <Card.Header>
        <Card.Title className="text-base">Energy Activity</Card.Title>
      </Card.Header>
      <Card.Content className="flex items-center gap-4">
        <div className="flex flex-1 flex-col gap-2 self-start">
          {energyData.map((item) => (
            <div key={item.name} className="flex flex-col">
              <span className="text-xs text-muted">{item.name}</span>
              <span className="text-sm font-semibold text-foreground">
                {item.valueText}
              </span>
            </div>
          ))}
        </div>
        <div className="relative shrink-0">
          <RadialChart
            data={energyData}
            height={200}
            innerRadius="40%"
            outerRadius="100%"
            width={200}
          >
            <RadialChart.Bar background cornerRadius={12} dataKey="value" />
            <RadialChart.Tooltip content={<RadialTooltip />} />
          </RadialChart>
          <div className="pointer-events-none absolute inset-0 flex flex-col items-center justify-center">
            <span className="text-[10px] text-muted">Calories</span>
            <span className="text-sm font-semibold text-foreground">
              700 kcal
            </span>
          </div>
        </div>
      </Card.Content>
    </Card>
  );
}
```
