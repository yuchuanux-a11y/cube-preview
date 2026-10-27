# TagGroup

A focusable list of tags with support for keyboard navigation, selection, and removal

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { TagGroup } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | — |
| `variant` | `"default" \| "surface"` | 否 | `—` | — |
| `children` | `React.ReactNode` | 否 | `—` | The children of the component. |
| `className` | `string` | 否 | `'react-aria-TagGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. |
| `defaultSelectedKeys` | `"all" \| Iterable<Key>` | 否 | `—` | The initial selected keys in the collection (uncontrolled). |
| `disabledKeys` | `Iterable<Key>` | 否 | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `disallowEmptySelection` | `boolean` | 否 | `—` | Whether the collection allows empty selection. |
| `escapeKeyBehavior` | `"none" \| "clearSelection"` | 否 | `'clearSelection'` | Whether pressing the escape key should clear selection in the TagGroup or not. Most experiences should not modify this option as it eliminates a keyboard user's ability to easily clear selection. Only use if the escape key is being handled externally or should not trigger selection clearing contextually. |
| `render` | `DOMRenderFunction<"div", undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKeys` | `"all" \| Iterable<Key>` | 否 | `—` | The currently selected keys in the collection (controlled). |
| `selectionBehavior` | `SelectionBehavior` | 否 | `'toggle'` | How multiple selection should behave in the collection. |
| `selectionMode` | `SelectionMode` | 否 | `—` | The type of selection that is allowed in the collection. |
| `shouldSelectOnPressUp` | `boolean` | 否 | `—` | Whether selection should occur on press up instead of press down. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `React.CSSProperties` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onAction` | `(key: Key) => void` | 否 | `—` | Handler that is called when a user performs an action on an item. The exact user event depends on the collection's `selectionBehavior` prop and the interaction modality. |
| `onRemove` | `(keys: Set<Key>) => void` | 否 | `—` | Handler that is called when a user deletes a tag. |
| `onSelectionChange` | `(keys: Selection) => void` | 否 | `—` | Handler that is called when the selection changes. |

</details>

## Parts

- `TagGroup.List`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=14288-4550

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/TagGroup
