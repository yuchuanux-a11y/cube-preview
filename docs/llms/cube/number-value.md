# NumberValue

Cube component `NumberValue` from `@bosagent/cube-ui/number-value`.

Cube component. Source: `packages/cube-ui/src/components/number-value`.

## Import

```tsx
import { NumberValue } from "@bosagent/cube-ui/number-value";
import { NumberValue } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
