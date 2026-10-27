# ChartTooltip

Cube component `ChartTooltip` from `@bosagent/cube-ui/chart-tooltip`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/chart-tooltip` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/chart-tooltip` |

检索：ChartTooltip、chart-tooltip。

## Import

```tsx
import { ChartTooltip } from "@bosagent/cube-ui/chart-tooltip";
import { ChartTooltip } from "@bosagent/cube-ui";
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

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ChartTooltip](https://yuchuanux-a11y.github.io/cube-preview/#ChartTooltip)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/chart-tooltip.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

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
