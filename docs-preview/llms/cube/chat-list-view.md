# ChatListView

Cube component `ChatListView` from `@bosagent/cube-ui/chat-list-view`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/chat-list-view` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/chat-list-view` |

检索：ChatListView、chat-list-view。

## Import

```tsx
import { ChatListView } from "@bosagent/cube-ui/chat-list-view";
import { ChatListView } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## 适用

建设中。设计 registry 没有这条用法。

## 不适用

建设中。

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `density` | `"compact" \| "comfortable"` | No | `—` | — |
| `renderEmptyState` | `() => ReactNode` | No | `—` | Render function for the empty state. |
| `rowHeight` | `number` | No | `48` | Estimated row height in pixels for virtualization. |
| `virtualized` | `boolean` | No | `false` | Enable row virtualization for large datasets. |
| `autoFocus` | `boolean \| FocusStrategy` | No | `—` | Whether to auto focus the gridlist or an option. |
| `children` | `React.ReactNode \| ((item: T) => ReactNode)` | No | `—` | The contents of the collection. |
| `className` | `ClassNameOrFunction<GridListRenderProps>` | No | `'react-aria-GridList'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultSelectedKeys` | `"all" \| Iterable<Key>` | No | `—` | The initial selected keys in the collection (uncontrolled). |
| `dependencies` | `readonly any[]` | No | `—` | Values that should invalidate the item cache when using dynamic collections. |
| `disabledBehavior` | `DisabledBehavior` | No | `'all'` | Whether `disabledKeys` applies to all interactions, or only selection. |
| `disabledKeys` | `Iterable<Key>` | No | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `disallowEmptySelection` | `boolean` | No | `—` | Whether the collection allows empty selection. |
| `disallowTypeAhead` | `boolean` | No | `false` | Whether typeahead navigation is disabled. |
| `dragAndDropHooks` | `DragAndDropHooks<NoInfer<T>>` | No | `—` | The drag and drop hooks returned by `useDragAndDrop` used to enable drag and drop behavior for the GridList. |
| `escapeKeyBehavior` | `"none" \| "clearSelection"` | No | `'clearSelection'` | Whether pressing the escape key should clear selection in the grid list or not. Most experiences should not modify this option as it eliminates a keyboard user's ability to easily clear selection. Only use if the escape key is being handled externally or should not trigger selection clearing contextually. |
| `items` | `Iterable<T>` | No | `—` | Item objects in the collection. |
| `keyboardNavigationBehavior` | `"tab" \| "arrow"` | No | `'arrow'` | Whether keyboard navigation to focusable elements within grid list items is via the left/right arrow keys or the tab key. |
| `onAction` | `(key: Key) => void` | No | `—` | Handler that is called when a user performs an action on an item. The exact user event depends on the collection's `selectionBehavior` prop and the interaction modality. |
| `onSelectionChange` | `(keys: Selection) => void` | No | `—` | Handler that is called when the selection changes. |
| `render` | `DOMRenderFunction<"div", GridListRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKeys` | `"all" \| Iterable<Key>` | No | `—` | The currently selected keys in the collection (controlled). |
| `selectionBehavior` | `SelectionBehavior` | No | `'toggle'` | How multiple selection should behave in the collection. |
| `selectionMode` | `SelectionMode` | No | `—` | The type of selection that is allowed in the collection. |
| `shouldSelectOnPressUp` | `boolean` | No | `—` | Whether selection should occur on press up instead of press down. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<GridListRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `UNSTABLE_focusOnEntry` | `"first" \| "last"` | No | `—` | Which item in the collection to focus when tabbing into the collection. Overrides default roving tab index like behavior. |

## Parts

- `ChatListView.Icon`
- `ChatListView.Item`
- `ChatListView.ItemContent`
- `ChatListView.Meta`
- `ChatListView.Preview`
- `ChatListView.Text`
- `ChatListView.Title`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ChatListView](https://yuchuanux-a11y.github.io/cube-preview/#ChatListView)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/chat-list-view.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { ChatListView } from '@components/chat-list-view';
import { Comment } from '@gravity-ui/icons';

const THREADS = [
  {
    id: '1',
    preview: 'Can you help me draft a launch checklist?',
    title: 'Product launch planning',
    updatedAt: '2h ago',
  },
  {
    id: '2',
    preview: 'Summarize the customer feedback from last week.',
    title: 'Customer feedback review',
    updatedAt: 'Yesterday',
  },
  {
    id: '3',
    preview: 'Rewrite this paragraph to sound more concise.',
    title: 'Copy editing help',
    updatedAt: 'Mon',
  },
] as const;

export function Default() {
  return (
    <div className="w-[480px]">
      <ChatListView aria-label="Recent chats" items={THREADS}>
        {(thread) => (
          <ChatListView.Item
            id={thread.id}
            textValue={`${thread.title} ${thread.preview}`}
          >
            <ChatListView.ItemContent>
              <ChatListView.Icon>
                <Comment />
              </ChatListView.Icon>
              <ChatListView.Text>
                <ChatListView.Title>{thread.title}</ChatListView.Title>
                <ChatListView.Preview>{thread.preview}</ChatListView.Preview>
              </ChatListView.Text>
              <ChatListView.Meta>{thread.updatedAt}</ChatListView.Meta>
            </ChatListView.ItemContent>
          </ChatListView.Item>
        )}
      </ChatListView>
    </div>
  );
}

export function Compact() {
  return (
    <div className="w-[280px]">
      <ChatListView aria-label="Recent chats" density="compact" items={THREADS}>
        {(thread) => (
          <ChatListView.Item id={thread.id} textValue={thread.title}>
            <ChatListView.ItemContent>
              <ChatListView.Icon>
                <Comment />
              </ChatListView.Icon>
              <ChatListView.Text>
                <ChatListView.Title>{thread.title}</ChatListView.Title>
                <ChatListView.Preview>{thread.preview}</ChatListView.Preview>
              </ChatListView.Text>
              <ChatListView.Meta>{thread.updatedAt}</ChatListView.Meta>
            </ChatListView.ItemContent>
          </ChatListView.Item>
        )}
      </ChatListView>
    </div>
  );
}
```
