# AppLayout

Cube component `AppLayout` from `@bosagent/cube-ui/app-layout`.

- 分层：Cube
- 包：`@bosagent/cube-ui/app-layout`
- 状态：建设中

## Import

```tsx
import { AppLayout } from "@bosagent/cube-ui/app-layout";
import { AppLayout } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | 是 | `—` | — |
| `aside` | `React.ReactNode` | 否 | `—` | — |
| `asideDefaultSize` | `ResizableSize` | 否 | `20` | Default size of the aside when resizable. Numbers are percentages; strings accept CSS units. |
| `asideMaxSize` | `ResizableSize` | 否 | `40` | Max aside size when resizable. Numbers are percentages; strings accept CSS units. |
| `asideMinSize` | `ResizableSize` | 否 | `15` | Min aside size when resizable. Numbers are percentages; strings accept CSS units. |
| `asideMobile` | `"hidden" \| "sheet"` | 否 | `—` | — |
| `asideOpen` | `boolean` | 否 | `—` | — |
| `asideResizable` | `boolean` | 否 | `—` | — |
| `asideResizeBehavior` | `ResizablePanelGroupResizeBehavior` | 否 | `"preserve-relative-size"` | How the aside panel behaves when the layout width changes. |
| `asideToggleShortcut` | `string \| false` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `defaultAsideOpen` | `boolean` | 否 | `—` | — |
| `defaultSidebarOpen` | `boolean` | 否 | `—` | — |
| `footer` | `React.ReactNode` | 否 | `—` | — |
| `navbar` | `React.ReactNode` | 否 | `—` | — |
| `navigate` | `SidebarNavigate` | 否 | `—` | — |
| `reduceMotion` | `boolean` | 否 | `—` | — |
| `resizableAutoSaveId` | `string` | 否 | `—` | — |
| `scrollMode` | `AppLayoutScrollMode` | 否 | `—` | — |
| `sidebar` | `React.ReactNode` | 否 | `—` | — |
| `sidebarCollapsible` | `"none" \| "icon" \| "offcanvas"` | 否 | `—` | — |
| `sidebarDefaultSize` | `ResizableSize` | 否 | `18` | Default size of the sidebar when resizable. Numbers are percentages; strings accept CSS units. |
| `sidebarMaxSize` | `ResizableSize` | 否 | `30` | Max sidebar size when resizable. Numbers are percentages; strings accept CSS units. |
| `sidebarMinSize` | `ResizableSize` | 否 | `12` | Min sidebar size when resizable. Numbers are percentages; strings accept CSS units. |
| `sidebarOpen` | `boolean` | 否 | `—` | — |
| `sidebarResizable` | `boolean` | 否 | `—` | — |
| `sidebarResizeBehavior` | `ResizablePanelGroupResizeBehavior` | 否 | `"preserve-relative-size"` | How the sidebar panel behaves when the layout width changes. |
| `sidebarSide` | `"left" \| "right"` | 否 | `—` | — |
| `sidebarVariant` | `"inset" \| "sidebar" \| "floating"` | 否 | `—` | — |
| `style` | `React.CSSProperties` | 否 | `—` | — |
| `toggleShortcut` | `string \| false` | 否 | `—` | — |
| `toolbar` | `React.ReactNode` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onAsideOpenChange` | `(open: boolean) => void` | 否 | `—` | — |
| `onSidebarOpenChange` | `(open: boolean) => void` | 否 | `—` | — |

</details>

## Parts

- `AppLayout.AsideTrigger`
- `AppLayout.MenuToggle`
- `AppLayout.MobileAside`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#AppLayout
