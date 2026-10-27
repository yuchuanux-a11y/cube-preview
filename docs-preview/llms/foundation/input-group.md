# InputGroup

Group related input controls with prefix and suffix elements for enhanced form fields

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { InputGroup } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | 否 | `—` | — |
| `variant` | `"primary" \| "secondary"` | 否 | `—` | — |
| `children` | `ChildrenOrFunction<GroupRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<GroupRenderProps>` | 否 | `'react-aria-Group'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the group is disabled. |
| `isInvalid` | `boolean` | 否 | `—` | Whether the group is invalid. |
| `isReadOnly` | `boolean` | 否 | `—` | Whether the group is read only. |
| `render` | `DOMRenderFunction<"div", GroupRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `role` | `"group" \| "presentation" \| "region"` | 否 | `'group'` | An accessibility role for the group. By default, this is set to `'group'`. Use `'region'` when the contents of the group is important enough to be included in the page table of contents. Use `'presentation'` if the group is visual only and does not represent a semantic grouping of controls. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<GroupRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onHoverChange` | `(isHovering: boolean) => void` | 否 | `—` | Handler that is called when the hover state changes. |
| `onHoverEnd` | `(e: HoverEvent) => void` | 否 | `—` | Handler that is called when a hover interaction ends. |
| `onHoverStart` | `(e: HoverEvent) => void` | 否 | `—` | Handler that is called when a hover interaction starts. |

</details>

## Parts

- `InputGroup.Input`
- `InputGroup.Prefix`
- `InputGroup.Suffix`
- `InputGroup.TextArea`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-29953

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/InputGroup
