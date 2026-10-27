# ListBox

A listbox displays a list of options and allows a user to select one or more of them

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { ListBox } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `className` | `string` | 否 | `'react-aria-ListBox'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `variant` | `"default" \| "danger"` | 否 | `—` | — |
| `autoFocus` | `boolean \| FocusStrategy` | 否 | `—` | Whether to auto focus the listbox or an option. |
| `children` | `React.ReactNode \| ((item: T) => ReactNode)` | 否 | `—` | The contents of the collection. |
| `defaultSelectedKeys` | `"all" \| Iterable<Key>` | 否 | `—` | The initial selected keys in the collection (uncontrolled). |
| `dependencies` | `readonly any[]` | 否 | `—` | Values that should invalidate the item cache when using dynamic collections. |
| `disabledKeys` | `Iterable<Key>` | 否 | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `disallowEmptySelection` | `boolean` | 否 | `—` | Whether the collection allows empty selection. |
| `dragAndDropHooks` | `DragAndDropHooks<NoInfer<T>>` | 否 | `—` | The drag and drop hooks returned by `useDragAndDrop` used to enable drag and drop behavior for the ListBox. |
| `escapeKeyBehavior` | `"none" \| "clearSelection"` | 否 | `'clearSelection'` | Whether pressing the escape key should clear selection in the listbox or not. Most experiences should not modify this option as it eliminates a keyboard user's ability to easily clear selection. Only use if the escape key is being handled externally or should not trigger selection clearing contextually. |
| `items` | `Iterable<T>` | 否 | `—` | Item objects in the collection. |
| `layout` | `"grid" \| "stack"` | 否 | `'stack'` | Whether the items are arranged in a stack or grid. |
| `orientation` | `Orientation` | 否 | `'vertical'` | The primary orientation of the items. Usually this is the direction that the collection scrolls. |
| `render` | `DOMRenderFunction<"div", ListBoxRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `renderEmptyState` | `(props: ListBoxRenderProps) => ReactNode` | 否 | `—` | Provides content to display when there are no items in the list. |
| `selectedKeys` | `"all" \| Iterable<Key>` | 否 | `—` | The currently selected keys in the collection (controlled). |
| `selectionBehavior` | `SelectionBehavior` | 否 | `'toggle'` | How multiple selection should behave in the collection. |
| `selectionMode` | `SelectionMode` | 否 | `—` | The type of selection that is allowed in the collection. |
| `shouldFocusOnHover` | `boolean` | 否 | `—` | Whether options should be focused when the user hovers over them. |
| `shouldFocusWrap` | `boolean` | 否 | `—` | Whether focus should wrap around when the end/start is reached. |
| `shouldSelectOnPressUp` | `boolean` | 否 | `—` | Whether selection should occur on press up instead of press down. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ListBoxRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onAction` | `(key: Key) => void` | 否 | `—` | Handler that is called when a user performs an action on an item. The exact user event depends on the collection's `selectionBehavior` prop and the interaction modality. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element loses focus. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | 否 | `—` | Handler that is called when the element's focus status changes. |
| `onSelectionChange` | `(keys: Selection) => void` | 否 | `—` | Handler that is called when the selection changes. |

</details>

## Parts

- `ListBox.Item`
- `ListBox.ItemIndicator`
- `ListBox.Section`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-70869
