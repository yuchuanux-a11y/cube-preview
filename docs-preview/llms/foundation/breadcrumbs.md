# Breadcrumbs

Navigation breadcrumbs showing the current page's location within a hierarchy

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Breadcrumbs } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `separator` | `React.ReactNode` | 否 | `—` | — |
| `children` | `React.ReactNode \| ((item: unknown) => ReactNode)` | 否 | `—` | The contents of the collection. |
| `className` | `string` | 否 | `'react-aria-Breadcrumbs'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. |
| `dependencies` | `readonly any[]` | 否 | `—` | Values that should invalidate the item cache when using dynamic collections. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the breadcrumbs are disabled. |
| `items` | `Iterable<unknown>` | 否 | `—` | Item objects in the collection. |
| `render` | `DOMRenderFunction<"ol", undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `React.CSSProperties` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onAction` | `(key: Key) => void` | 否 | `—` | Handler that is called when a breadcrumb is clicked. |

</details>

## Parts

- `Breadcrumbs.Item`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=14153-3704
