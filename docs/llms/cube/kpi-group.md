# KPIGroup

Cube component `KPIGroup` from `@bosagent/cube-ui/kpi-group`.

Cube component. Source: `packages/cube-ui/src/components/kpi-group`.

## Import

```tsx
import { KPIGroup } from "@bosagent/cube-ui/kpi-group";
import { KPIGroup } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `orientation` | `"horizontal" \| "vertical"` | No | `"horizontal"` | Layout direction. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `KPIGroup.Separator`

## Example source

```tsx
'use client';

import { KPI } from '@components/kpi';
import { KPIGroup } from '@components/kpi-group';

export function Horizontal() {
  return (
    <div className="w-[900px] rounded-2xl p-6">
      <KPIGroup>
        <KPI>
          <KPI.Header>
            <KPI.Title>Total Subscribers</KPI.Title>
          </KPI.Header>
          <KPI.Content>
            <KPI.Value maximumFractionDigits={0} value={71897} />
            <KPI.Trend trend="up">12%</KPI.Trend>
          </KPI.Content>
        </KPI>
        <KPIGroup.Separator />
        <KPI>
          <KPI.Header>
            <KPI.Title>Avg. Open Rate</KPI.Title>
          </KPI.Header>
          <KPI.Content>
            <KPI.Value
              maximumFractionDigits={2}
              style="percent"
              value={0.5816}
            />
            <KPI.Trend trend="up">2.02%</KPI.Trend>
          </KPI.Content>
        </KPI>
        <KPIGroup.Separator />
        <KPI>
          <KPI.Header>
            <KPI.Title>Avg. Click Rate</KPI.Title>
          </KPI.Header>
          <KPI.Content>
            <KPI.Value
              maximumFractionDigits={2}
              style="percent"
              value={0.2457}
            />
            <KPI.Trend trend="down">4.05%</KPI.Trend>
          </KPI.Content>
        </KPI>
      </KPIGroup>
    </div>
  );
}
```
