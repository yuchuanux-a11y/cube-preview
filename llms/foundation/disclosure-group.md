# DisclosureGroup

Container that manages multiple Disclosure items with coordinated expanded states

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { DisclosureGroup } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `allowsMultipleExpanded` | `boolean` | 否 | `—` | Whether multiple items can be expanded at the same time. |
| `children` | `ChildrenOrFunction<DisclosureGroupRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<DisclosureGroupRenderProps>` | 否 | `'react-aria-DisclosureGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultExpandedKeys` | `Iterable<Key>` | 否 | `—` | The initial expanded keys in the group (uncontrolled). |
| `expandedKeys` | `Iterable<Key>` | 否 | `—` | The currently expanded keys in the group (controlled). |
| `isDisabled` | `boolean` | 否 | `—` | Whether all items are disabled. |
| `render` | `DOMRenderFunction<"div", DisclosureGroupRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `style` | `StyleOrFunction<DisclosureGroupRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onExpandedChange` | `(keys: Set<Key>) => any` | 否 | `—` | Handler that is called when items are expanded or collapsed. |

</details>

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-43646
