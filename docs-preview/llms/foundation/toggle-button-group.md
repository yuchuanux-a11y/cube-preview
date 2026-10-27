# ToggleButtonGroup

Groups multiple ToggleButtons into a unified control, allowing users to select one or multiple options.

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { ToggleButtonGroup } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | 否 | `—` | — |
| `isDetached` | `boolean` | 否 | `—` | Whether the group buttons are visually separated (detached) instead of connected |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | Size to propagate to all child ToggleButtons |
| `children` | `ChildrenOrFunction<ToggleButtonGroupRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ToggleButtonGroupRenderProps>` | 否 | `'react-aria-ToggleButtonGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultSelectedKeys` | `Iterable<Key>` | 否 | `—` | The initial selected keys in the collection (uncontrolled). |
| `disallowEmptySelection` | `boolean` | 否 | `—` | Whether the collection allows empty selection. |
| `isDisabled` | `boolean` | 否 | `—` | Whether all items are disabled. |
| `orientation` | `Orientation` | 否 | `'horizontal'` | The orientation of the the toggle button group. |
| `render` | `DOMRenderFunction<"div", ToggleButtonGroupRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKeys` | `Iterable<Key>` | 否 | `—` | The currently selected keys in the collection (controlled). |
| `selectionMode` | `"single" \| "multiple"` | 否 | `'single'` | Whether single or multiple selection is enabled. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ToggleButtonGroupRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onSelectionChange` | `(keys: Set<Key>) => void` | 否 | `—` | Handler that is called when the selection changes. |

</details>

## Parts

- `ToggleButtonGroup.Separator`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=15251-25651
