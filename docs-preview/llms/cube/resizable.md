# Resizable

Cube component `Resizable` from `@bosagent/cube-ui/resizable`.

- 分层：Cube
- 包：`@bosagent/cube-ui/resizable`
- 状态：建设中

## Import

```tsx
import { Resizable } from "@bosagent/cube-ui/resizable";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | 是 | `—` | — |
| `autoSaveId` | `string` | 否 | `—` | — |
| `handleRef` | `React.Ref<GroupImperativeHandle>` | 否 | `—` | — |
| `id` | `string` | 否 | `—` | — |
| `orientation` | `"horizontal" \| "vertical"` | 否 | `—` | — |
| `storage` | `LayoutStorage` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onLayoutChange` | `(layout: Layout) => void` | 否 | `—` | — |

</details>

## Parts

- `Resizable.Handle`
- `Resizable.Indicator`
- `Resizable.Panel`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=16902-29717

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Resizable
