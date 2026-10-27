# KPI

Cube component `KPI` from `@bosagent/cube-ui/kpi`.

- 分层：Cube
- 包：`@bosagent/cube-ui/kpi`
- 状态：建设中

## Import

```tsx
import { KPI } from "@bosagent/cube-ui/kpi";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `render` | `DOMRenderFunction<keyof React.JSX.IntrinsicElements, undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `variant` | `"default" \| "secondary" \| "tertiary" \| "transparent"` | 否 | `"default"` | Visual variant. |
| `slot` | `string` | 否 | `—` | — |

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

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#KPI
