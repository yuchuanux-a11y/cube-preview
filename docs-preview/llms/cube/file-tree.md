# FileTree

Cube component `FileTree` from `@bosagent/cube-ui/file-tree`.

- 分层：Cube
- 包：`@bosagent/cube-ui/file-tree`
- 状态：建设中

## Import

```tsx
import { FileTree } from "@bosagent/cube-ui/file-tree";
import { FileTree } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `reduceMotion` | `boolean` | 否 | `false` | Whether to disable expand/collapse animations. Also respects the user's reduced-motion preference. |
| `showGuideLines` | `boolean \| "hover"` | 否 | `true` | Whether to show indent guide lines. `true` = always, `false` = never, `"hover"` = on tree hover only. |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `"md"` | Size variant. |
| `autoFocus` | `boolean \| FocusStrategy` | 否 | `—` | Whether to auto focus the gridlist or an option. |
| `children` | `React.ReactNode \| ((item: T) => ReactNode)` | 否 | `—` | The contents of the collection. |
| `className` | `ClassNameOrFunction<TreeRenderProps>` | 否 | `'react-aria-Tree'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultExpandedKeys` | `Iterable<Key>` | 否 | `—` | The initial expanded keys in the collection (uncontrolled). |
| `defaultSelectedKeys` | `"all" \| Iterable<Key>` | 否 | `—` | The initial selected keys in the collection (uncontrolled). |
| `dependencies` | `readonly any[]` | 否 | `—` | Values that should invalidate the item cache when using dynamic collections. |
| `disabledBehavior` | `DisabledBehavior` | 否 | `'all'` | Whether `disabledKeys` applies to all interactions, or only selection. |
| `disabledKeys` | `Iterable<Key>` | 否 | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `disallowEmptySelection` | `boolean` | 否 | `—` | Whether the collection allows empty selection. |
| `dragAndDropHooks` | `DragAndDropHooks<NoInfer<T>>` | 否 | `—` | The drag and drop hooks returned by `useDragAndDrop` used to enable drag and drop behavior for the Tree. |
| `escapeKeyBehavior` | `"none" \| "clearSelection"` | 否 | `'clearSelection'` | Whether pressing the escape key should clear selection in the grid list or not. Most experiences should not modify this option as it eliminates a keyboard user's ability to easily clear selection. Only use if the escape key is being handled externally or should not trigger selection clearing contextually. |
| `expandedKeys` | `Iterable<Key>` | 否 | `—` | The currently expanded keys in the collection (controlled). |
| `items` | `Iterable<T>` | 否 | `—` | Item objects in the collection. |
| `keyboardNavigationBehavior` | `"tab" \| "arrow"` | 否 | `'arrow'` | Whether keyboard navigation to focusable elements within grid list items is via the left/right arrow keys or the tab key. |
| `render` | `DOMRenderFunction<"div", TreeRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `renderEmptyState` | `(props: TreeEmptyStateRenderProps) => ReactNode` | 否 | `—` | Provides content to display when there are no items in the list. |
| `selectedKeys` | `"all" \| Iterable<Key>` | 否 | `—` | The currently selected keys in the collection (controlled). |
| `selectionBehavior` | `SelectionBehavior` | 否 | `'toggle'` | How multiple selection should behave in the tree. |
| `selectionMode` | `SelectionMode` | 否 | `—` | The type of selection that is allowed in the collection. |
| `shouldSelectOnPressUp` | `boolean` | 否 | `—` | Whether selection should occur on press up instead of press down. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<TreeRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onAction` | `(key: Key) => void` | 否 | `—` | Handler that is called when a user performs an action on an item. The exact user event depends on the collection's `selectionBehavior` prop and the interaction modality. |
| `onExpandedChange` | `(keys: Set<Key>) => any` | 否 | `—` | Handler that is called when items are expanded or collapsed. |
| `onSelectionChange` | `(keys: Selection) => void` | 否 | `—` | Handler that is called when the selection changes. |

</details>

## Parts

- `FileTree.Header`
- `FileTree.Indicator`
- `FileTree.Item`
- `FileTree.Section`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#FileTree
