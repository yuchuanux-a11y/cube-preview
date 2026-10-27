# FileTree

Cube component `FileTree` from `@bosagent/cube-ui/file-tree`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/file-tree` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/file-tree` |

检索：FileTree、file-tree。

## Import

```tsx
import { FileTree } from "@bosagent/cube-ui/file-tree";
import { FileTree } from "@bosagent/cube-ui";
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
| `reduceMotion` | `boolean` | No | `false` | Whether to disable expand/collapse animations. Also respects the user's reduced-motion preference. |
| `showGuideLines` | `boolean \| "hover"` | No | `true` | Whether to show indent guide lines. `true` = always, `false` = never, `"hover"` = on tree hover only. |
| `size` | `"md" \| "lg" \| "sm"` | No | `"md"` | Size variant. |
| `autoFocus` | `boolean \| FocusStrategy` | No | `—` | Whether to auto focus the gridlist or an option. |
| `children` | `React.ReactNode \| ((item: T) => ReactNode)` | No | `—` | The contents of the collection. |
| `className` | `ClassNameOrFunction<TreeRenderProps>` | No | `'react-aria-Tree'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultExpandedKeys` | `Iterable<Key>` | No | `—` | The initial expanded keys in the collection (uncontrolled). |
| `defaultSelectedKeys` | `"all" \| Iterable<Key>` | No | `—` | The initial selected keys in the collection (uncontrolled). |
| `dependencies` | `readonly any[]` | No | `—` | Values that should invalidate the item cache when using dynamic collections. |
| `disabledBehavior` | `DisabledBehavior` | No | `'all'` | Whether `disabledKeys` applies to all interactions, or only selection. |
| `disabledKeys` | `Iterable<Key>` | No | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `disallowEmptySelection` | `boolean` | No | `—` | Whether the collection allows empty selection. |
| `dragAndDropHooks` | `DragAndDropHooks<NoInfer<T>>` | No | `—` | The drag and drop hooks returned by `useDragAndDrop` used to enable drag and drop behavior for the Tree. |
| `escapeKeyBehavior` | `"none" \| "clearSelection"` | No | `'clearSelection'` | Whether pressing the escape key should clear selection in the grid list or not. Most experiences should not modify this option as it eliminates a keyboard user's ability to easily clear selection. Only use if the escape key is being handled externally or should not trigger selection clearing contextually. |
| `expandedKeys` | `Iterable<Key>` | No | `—` | The currently expanded keys in the collection (controlled). |
| `items` | `Iterable<T>` | No | `—` | Item objects in the collection. |
| `keyboardNavigationBehavior` | `"tab" \| "arrow"` | No | `'arrow'` | Whether keyboard navigation to focusable elements within grid list items is via the left/right arrow keys or the tab key. |
| `onAction` | `(key: Key) => void` | No | `—` | Handler that is called when a user performs an action on an item. The exact user event depends on the collection's `selectionBehavior` prop and the interaction modality. |
| `onExpandedChange` | `(keys: Set<Key>) => any` | No | `—` | Handler that is called when items are expanded or collapsed. |
| `onSelectionChange` | `(keys: Selection) => void` | No | `—` | Handler that is called when the selection changes. |
| `render` | `DOMRenderFunction<"div", TreeRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `renderEmptyState` | `(props: TreeEmptyStateRenderProps) => ReactNode` | No | `—` | Provides content to display when there are no items in the list. |
| `selectedKeys` | `"all" \| Iterable<Key>` | No | `—` | The currently selected keys in the collection (controlled). |
| `selectionBehavior` | `SelectionBehavior` | No | `'toggle'` | How multiple selection should behave in the tree. |
| `selectionMode` | `SelectionMode` | No | `—` | The type of selection that is allowed in the collection. |
| `shouldSelectOnPressUp` | `boolean` | No | `—` | Whether selection should occur on press up instead of press down. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<TreeRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `FileTree.Header`
- `FileTree.Indicator`
- `FileTree.Item`
- `FileTree.Section`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[FileTree](https://yuchuanux-a11y.github.io/cube-preview/#FileTree)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/file-tree.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { FileTree } from '@components/file-tree';

export function Default() {
  return (
    <FileTree
      aria-label="Project structure"
      className="max-h-[420px] w-80"
      defaultExpandedKeys={[
        'apps',
        'frontend',
        'api',
        'packages',
        'packages-react',
        'claude',
      ]}
    >
      <FileTree.Item id="apps" textValue="apps" title="apps">
        <FileTree.Item id="frontend" textValue="frontend" title="frontend">
          <FileTree.Item
            id="fe-package"
            textValue="package.json"
            title="package.json"
          />
          <FileTree.Item
            id="fe-tsconfig"
            textValue="tsconfig.json"
            title="tsconfig.json"
          />
          <FileTree.Item id="fe-src" textValue="src" title="src">
            <FileTree.Item id="fe-app" textValue="app" title="app">
              <FileTree.Item
                id="fe-layout"
                textValue="layout.tsx"
                title="layout.tsx"
              />
              <FileTree.Item
                id="fe-page"
                textValue="page.tsx"
                title="page.tsx"
              />
            </FileTree.Item>
          </FileTree.Item>
        </FileTree.Item>
        <FileTree.Item id="api" textValue="api" title="api">
          <FileTree.Item
            id="api-package"
            textValue="package.json"
            title="package.json"
          />
          <FileTree.Item id="api-src" textValue="src" title="src">
            <FileTree.Item
              id="api-index"
              textValue="index.ts"
              title="index.ts"
            />
            <FileTree.Item
              id="api-routes"
              textValue="routes.ts"
              title="routes.ts"
            />
          </FileTree.Item>
        </FileTree.Item>
      </FileTree.Item>
      <FileTree.Item id="packages" textValue="packages" title="packages">
        <FileTree.Item id="packages-react" textValue="react" title="react">
          <FileTree.Item
            id="pr-package"
            textValue="package.json"
            title="package.json"
          />
          <FileTree.Item id="pr-src" textValue="src" title="src">
            <FileTree.Item
              id="pr-components"
              textValue="components"
              title="components"
            >
              <FileTree.Item
                id="pr-index"
                textValue="index.ts"
                title="index.ts"
              />
            </FileTree.Item>
          </FileTree.Item>
        </FileTree.Item>
      </FileTree.Item>
      <FileTree.Item id="claude" textValue=".claude" title=".claude">
        <FileTree.Item id="claude-skills" textValue="skills" title="skills">
          <FileTree.Item
            id="skill-heroui"
            textValue="heroui-react"
            title="heroui-react"
          >
            <FileTree.Item
              id="skill-md"
              textValue="SKILL.md"
              title="SKILL.md"
            />
          </FileTree.Item>
        </FileTree.Item>
      </FileTree.Item>
      <FileTree.Item id="readme" textValue="README.md" title="README.md" />
      <FileTree.Item id="agents" textValue="AGENTS.md" title="AGENTS.md" />
      <FileTree.Item
        id="root-package"
        textValue="package.json"
        title="package.json"
      />
      <FileTree.Item
        id="root-tsconfig"
        textValue="tsconfig.json"
        title="tsconfig.json"
      />
    </FileTree>
  );
}
```
