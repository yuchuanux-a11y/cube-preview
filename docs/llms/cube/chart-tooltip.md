# ChartTooltip

Cube component `ChartTooltip` from `@bosagent/cube-ui/chart-tooltip`.

Cube component. Source: `packages/cube-ui/src/components/chart-tooltip`.

## Import

```tsx
import { ChartTooltip } from "@bosagent/cube-ui/chart-tooltip";
import { ChartTooltip } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `active` | `boolean` | No | `—` | Controls visibility. When false, the tooltip is not rendered. |
| `indicator` | `"line" \| "dot"` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `ChartTooltip.Content`
- `ChartTooltip.Header`
- `ChartTooltip.Indicator`
- `ChartTooltip.Item`
- `ChartTooltip.Label`
- `ChartTooltip.Value`

## Example source

```tsx
'use client';

import { ChartTooltip } from '@components/chart-tooltip';

export function Default() {
  return (
    <div className="flex gap-6">
      <ChartTooltip.Content
        active
        indicator="dot"
        label="February"
        payload={[
          { color: 'var(--chart-3)', name: 'Revenue', value: 18200 },
          { color: 'var(--chart-1)', name: 'Expenses', value: 9800 },
        ]}
      />
      <ChartTooltip.Content
        active
        indicator="line"
        label="Q1 2025"
        payload={[
          { name: 'Organic', stroke: 'var(--chart-3)', value: 22000 },
          { name: 'Paid Ads', stroke: 'var(--chart-2)', value: 14500 },
          { name: 'Referral', stroke: 'var(--chart-1)', value: 5200 },
        ]}
      />
    </div>
  );
}
```
