# FloatingToc

Cube component `FloatingToc` from `@bosagent/cube-ui/floating-toc`.

- 分层：Cube
- 包：`@bosagent/cube-ui/floating-toc`
- 状态：建设中

## Import

```tsx
import { FloatingToc } from "@bosagent/cube-ui/floating-toc";
import { FloatingToc } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `closeDelay` | `number` | 否 | `300` | Time in ms before the floating toc closes after pointer/focus leave. |
| `defaultOpen` | `boolean` | 否 | `—` | Default open state (uncontrolled). |
| `open` | `boolean` | 否 | `—` | Controlled open state. |
| `openDelay` | `number` | 否 | `200` | Time in ms before the floating toc opens after hover. |
| `placement` | `"left" \| "right"` | 否 | `"right"` | Which side of the page the TOC is on. Controls bar growth direction and default content side. |
| `triggerMode` | `"hover" \| "press"` | 否 | `"hover"` | How the trigger opens the content. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onOpenChange` | `(open: boolean) => void` | 否 | `—` | Callback when open state changes. |

</details>

## Parts

- `FloatingToc.Bar`
- `FloatingToc.Content`
- `FloatingToc.Item`
- `FloatingToc.Trigger`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#FloatingToc
