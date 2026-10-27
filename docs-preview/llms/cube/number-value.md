# NumberValue

Cube component `NumberValue` from `@bosagent/cube-ui/number-value`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/number-value` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/number-value` |

检索：NumberValue、number-value。

## Import

```tsx
import { NumberValue } from "@bosagent/cube-ui/number-value";
import { NumberValue } from "@bosagent/cube-ui";
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
| `value` | `number` | Yes | `—` | — |
| `children` | `React.ReactNode \| ((formatted: string) => ReactNode)` | No | `—` | Render prop receiving the formatted string, or ReactNode children (Prefix/Suffix). |
| `currency` | `string` | No | `—` | Currency code (e.g. "USD"). Required when style is "currency". |
| `formatOptions` | `NumberFormatOptions` | No | `—` | Format options. Overrides individual props. |
| `locale` | `string` | No | `—` | Override locale from I18nProvider. |
| `maximumFractionDigits` | `number` | No | `—` | — |
| `minimumFractionDigits` | `number` | No | `—` | — |
| `notation` | `"compact" \| "engineering" \| "scientific" \| "standard"` | No | `"standard"` | — |
| `signDisplay` | `"auto" \| "always" \| "never" \| "exceptZero"` | No | `—` | — |
| `style` | `"decimal" \| "unit" \| "currency" \| "percent"` | No | `"decimal"` | — |
| `unit` | `string` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `NumberValue.Prefix`
- `NumberValue.Suffix`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[NumberValue](https://yuchuanux-a11y.github.io/cube-preview/#NumberValue)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/number-value.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { NumberValue } from '@components/number-value';

export function Default() {
  return (
    <div className="flex flex-col gap-3 rounded-2xl p-6">
      <div className="flex items-baseline gap-4">
        <span className="w-12 text-xs text-muted">USD</span>
        <NumberValue
          className="text-2xl font-semibold text-foreground"
          currency="USD"
          style="currency"
          value={228441}
        />
      </div>
      <div className="flex items-baseline gap-4">
        <span className="w-12 text-xs text-muted">EUR</span>
        <NumberValue
          className="text-2xl font-semibold text-foreground"
          currency="EUR"
          style="currency"
          value={228441}
        />
      </div>
      <div className="flex items-baseline gap-4">
        <span className="w-12 text-xs text-muted">JPY</span>
        <NumberValue
          className="text-2xl font-semibold text-foreground"
          currency="JPY"
          maximumFractionDigits={0}
          style="currency"
          value={228441}
        />
      </div>
      <div className="flex items-baseline gap-4">
        <span className="w-12 text-xs text-muted">GBP</span>
        <NumberValue
          className="text-2xl font-semibold text-foreground"
          currency="GBP"
          style="currency"
          value={228441}
        />
      </div>
    </div>
  );
}
```
