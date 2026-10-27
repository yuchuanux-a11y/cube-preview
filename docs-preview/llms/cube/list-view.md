# ListView

Cube component `ListView` from `@bosagent/cube-ui/list-view`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/list-view` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/list-view` |

检索：ListView、list-view。

## Import

```tsx
import { ListView } from "@bosagent/cube-ui/list-view";
import { ListView } from "@bosagent/cube-ui";
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
| `renderEmptyState` | `() => ReactNode` | No | `—` | Render function for the empty state. |
| `rowHeight` | `number` | No | `48` | Estimated row height in pixels for virtualization. |
| `variant` | `"primary" \| "secondary"` | No | `"primary"` | Visual variant. |
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

- `ListView.Description`
- `ListView.Item`
- `ListView.ItemAction`
- `ListView.ItemContent`
- `ListView.Title`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ListView](https://yuchuanux-a11y.github.io/cube-preview/#ListView)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/list-view.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { useState } from 'react';
import type { Selection } from 'react-aria-components/GridList';
import { ListView } from '@components/list-view';
import { File, Folder } from '@gravity-ui/icons';

const files = [
  { icon: 'folder', id: '1', name: 'Documents', updated: '2 days ago' },
  { icon: 'folder', id: '2', name: 'Photos', updated: '1 week ago' },
  { icon: 'file', id: '3', name: 'README.md', updated: '3 hours ago' },
  { icon: 'file', id: '4', name: 'package.json', updated: 'Yesterday' },
  { icon: 'folder', id: '5', name: 'src', updated: 'Just now' },
  { icon: 'file', id: '6', name: '.gitignore', updated: '2 weeks ago' },
];

export function Default() {
  // eslint-disable-next-line @eslint-react/use-state
  const [selected, setSelected] = useState<Selection>(new Set());

  return (
    <div className="w-full max-w-md">
      <ListView
        aria-label="Files"
        items={files}
        selectedKeys={selected}
        selectionMode="multiple"
        variant="primary"
        onSelectionChange={setSelected}
      >
        {(file) => (
          <ListView.Item id={file.id} textValue={file.name}>
            <ListView.ItemContent>
              {file.icon === 'folder' ? <Folder /> : <File />}
              <div className="flex min-w-0 flex-col">
                <ListView.Title>{file.name}</ListView.Title>
                <ListView.Description>
                  Updated {file.updated}
                </ListView.Description>
              </div>
            </ListView.ItemContent>
          </ListView.Item>
        )}
      </ListView>
    </div>
  );
}
```
