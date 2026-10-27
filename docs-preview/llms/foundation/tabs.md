# Tabs

Tabs organize content into multiple sections and allow users to navigate between them.

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Tabs } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `align` | `"center" \| "end" \| "start"` | 否 | `—` | — |
| `className` | `string` | 否 | `'react-aria-Tabs'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `variant` | `"primary" \| "secondary"` | 否 | `—` | — |
| `defaultSelectedKey` | `Key` | 否 | `—` | The initial selected keys in the collection (uncontrolled). |
| `disabledKeys` | `Iterable<Key>` | 否 | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the TabList is disabled. Shows that a selection exists, but is not available in that circumstance. |
| `keyboardActivation` | `"manual" \| "automatic"` | 否 | `'automatic'` | Whether tabs are activated automatically on focus or manually. |
| `orientation` | `Orientation` | 否 | `'horizontal'` | The orientation of the tabs. |
| `render` | `DOMRenderFunction<"div", TabsRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKey` | `Key` | 否 | `—` | The currently selected key in the collection (controlled). |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<TabsRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onSelectionChange` | `(key: Key) => void` | 否 | `—` | Handler that is called when the selection changes. |

</details>

## Parts

- `Tabs.Indicator`
- `Tabs.List`
- `Tabs.ListContainer`
- `Tabs.Panel`
- `Tabs.Separator`
- `Tabs.Tab`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-79785

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Tabs
