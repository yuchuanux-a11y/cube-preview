# KPIGroup

Cube component `KPIGroup` from `@bosagent/cube-ui/kpi-group`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/kpi-group` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/kpi-group` |

检索：KPIGroup、kpi-group。

## Import

```tsx
import { KPIGroup } from "@bosagent/cube-ui/kpi-group";
import { KPIGroup } from "@bosagent/cube-ui";
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
| `orientation` | `"horizontal" \| "vertical"` | No | `"horizontal"` | Layout direction. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `KPIGroup.Separator`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[KPIGroup](https://yuchuanux-a11y.github.io/cube-preview/#KPIGroup)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/kpi-group.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

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
