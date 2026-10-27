# NumberValue

Cube component `NumberValue` from `@bosagent/cube-ui/number-value`.

- 分层：Cube
- 包：`@bosagent/cube-ui/number-value`
- 状态：建设中

## Import

```tsx
import { NumberValue } from "@bosagent/cube-ui/number-value";
import { NumberValue } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `value` | `number` | 是 | `—` | — |
| `children` | `React.ReactNode \| ((formatted: string) => ReactNode)` | 否 | `—` | Render prop receiving the formatted string, or ReactNode children (Prefix/Suffix). |
| `currency` | `string` | 否 | `—` | Currency code (e.g. "USD"). Required when style is "currency". |
| `formatOptions` | `NumberFormatOptions` | 否 | `—` | Format options. Overrides individual props. |
| `locale` | `string` | 否 | `—` | Override locale from I18nProvider. |
| `maximumFractionDigits` | `number` | 否 | `—` | — |
| `minimumFractionDigits` | `number` | 否 | `—` | — |
| `notation` | `"compact" \| "engineering" \| "scientific" \| "standard"` | 否 | `"standard"` | — |
| `signDisplay` | `"auto" \| "always" \| "never" \| "exceptZero"` | 否 | `—` | — |
| `style` | `"decimal" \| "unit" \| "currency" \| "percent"` | 否 | `"decimal"` | — |
| `unit` | `string` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

## Parts

- `NumberValue.Prefix`
- `NumberValue.Suffix`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#NumberValue
