# KPI

Cube component `KPI` from `@bosagent/cube-ui/kpi`.

Cube component. Source: `packages/cube-ui/src/components/kpi`.

## Import

```tsx
import { KPI } from "@bosagent/cube-ui/kpi";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<keyof React.JSX.IntrinsicElements, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `variant` | `"default" \| "secondary" \| "tertiary" \| "transparent"` | No | `"default"` | Visual variant. |
| `slot` | `string` | No | `—` | — |

## Parts

- `KPI.Actions`
- `KPI.Chart`
- `KPI.Content`
- `KPI.Footer`
- `KPI.Header`
- `KPI.Icon`
- `KPI.Progress`
- `KPI.Separator`
- `KPI.Title`
- `KPI.Trend`
- `KPI.Value`

## Example source

```tsx
'use client';

import { AreaChart } from '@components/area-chart';
import { ChartTooltip } from '@components/chart-tooltip';
import { KPI } from '@components/kpi';

const revenueCards = [
  {
    change: '+33%',
    title: 'Total Revenue',
    trend: 'up' as const,
    value: 228451,
  },
  {
    change: '+13.0%',
    title: 'Total Expenses',
    trend: 'down' as const,
    value: 71887,
  },
  {
    change: '0.0%',
    title: 'Total Profit',
    trend: 'neutral' as const,
    value: 156540,
  },
  {
    change: '+1.0%',
    title: 'New Customers',
    trend: 'up' as const,
    value: 1234,
  },
];

const sparkline = [
  { month: 'Jan', value: 4200 },
  { month: 'Feb', value: 5100 },
  { month: 'Mar', value: null },
  { month: 'Apr', value: 6200 },
  { month: 'May', value: 5900 },
  { month: 'Jun', value: 7100 },
];

export function Default() {
  return (
    <div className="flex flex-col gap-6 rounded-2xl p-6">
      <div className="grid grid-cols-1 gap-3 sm:grid-cols-2 lg:grid-cols-4">
        {revenueCards.map((card) => (
          <KPI key={card.title}>
            <KPI.Header>
              <KPI.Title>{card.title}</KPI.Title>
            </KPI.Header>
            <KPI.Content>
              <KPI.Value
                currency={card.title.includes('Customer') ? undefined : 'USD'}
                maximumFractionDigits={0}
                style={card.title.includes('Customer') ? 'decimal' : 'currency'}
                value={card.value}
              />
              <KPI.Trend trend={card.trend}>{card.change}</KPI.Trend>
            </KPI.Content>
          </KPI>
        ))}
      </div>

      <KPI className="max-w-sm">
        <KPI.Header>
          <KPI.Title>Monthly Revenue</KPI.Title>
        </KPI.Header>
        <KPI.Content>
          <KPI.Value currency="USD" maximumFractionDigits={0} value={7100} />
          <KPI.Trend trend="up">+12%</KPI.Trend>
        </KPI.Content>
        <KPI.Chart
          connectNulls
          color="var(--color-success)"
          data={sparkline}
          height={70}
          tooltip={
            <AreaChart.Tooltip
              content={({ active, payload }) => {
                const point = payload?.[0];

                if (!active || !point) return null;

                return (
                  <ChartTooltip>
                    <ChartTooltip.Header>
                      {point.payload?.month}
                    </ChartTooltip.Header>
                    <ChartTooltip.Item>
                      <ChartTooltip.Indicator color={point.stroke} />
                      <ChartTooltip.Label>Revenue</ChartTooltip.Label>
                      <ChartTooltip.Value>
                        ${Number(point.value).toLocaleString()}
                      </ChartTooltip.Value>
                    </ChartTooltip.Item>
                  </ChartTooltip>
                );
              }}
            />
          }
        />
      </KPI>
    </div>
  );
}
```
