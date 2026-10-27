# TrendChip

Cube component `TrendChip` from `@bosagent/cube-ui/trend-chip`.

- 分层：Cube
- 包：`@bosagent/cube-ui/trend-chip`
- 状态：建设中

## Import

```tsx
import { TrendChip } from "@bosagent/cube-ui/trend-chip";
import { TrendChip } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `render` | `DOMRenderFunction<keyof React.JSX.IntrinsicElements, undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | — |
| `trend` | `TrendType` | 否 | `—` | — |
| `variant` | `"primary" \| "secondary" \| "tertiary" \| "soft"` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

## Parts

- `TrendChip.Indicator`
- `TrendChip.Prefix`
- `TrendChip.Suffix`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#TrendChip
