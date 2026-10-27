# Navbar

Cube component `Navbar` from `@bosagent/cube-ui/navbar`.

- 分层：Cube
- 包：`@bosagent/cube-ui/navbar`
- 状态：建设中

## Import

```tsx
import { Navbar } from "@bosagent/cube-ui/navbar";
import { Navbar } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | 是 | `—` | — |
| `defaultMenuOpen` | `boolean` | 否 | `false` | Default menu open state (uncontrolled). |
| `height` | `string` | 否 | `"4rem"` | Navbar height CSS value. |
| `hideOnScroll` | `boolean` | 否 | `false` | Enable hide-on-scroll behavior. |
| `isMenuOpen` | `boolean` | 否 | `—` | Controlled menu open state. |
| `maxWidth` | `"md" \| "lg" \| "sm" \| "xl" \| "2xl" \| "full"` | 否 | `—` | — |
| `navigate` | `NavbarNavigate` | 否 | `—` | Programmatic navigation function for client-side routing (e.g. `router.push`). Called when an Item/MenuItem with `href` is pressed. When the `Navbar` is rendered inside an `AppLayout`, it automatically inherits the layout's `navigate` unless this prop is set. If omitted, the `Navbar` defers to a global React Aria `RouterProvider` when one is present, falling back to native browser navigation otherwise. |
| `parentRef` | `React.RefObject<HTMLElement>` | 否 | `window` | Scroll container ref for hide-on-scroll. |
| `position` | `"static" \| "sticky" \| "floating"` | 否 | `—` | — |
| `shouldBlockScroll` | `boolean` | 否 | `true` | Block background scroll when menu is open. |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onMenuOpenChange` | `(isOpen: boolean) => void` | 否 | `—` | Callback when menu open state changes. |

</details>

## Parts

- `Navbar.Brand`
- `Navbar.Content`
- `Navbar.Header`
- `Navbar.Item`
- `Navbar.Label`
- `Navbar.Menu`
- `Navbar.MenuItem`
- `Navbar.MenuToggle`
- `Navbar.Separator`
- `Navbar.Spacer`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Navbar
