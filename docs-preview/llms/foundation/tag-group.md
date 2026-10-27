# TagGroup

A focusable list of tags with support for keyboard navigation, selection, and removal

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：TagGroup、tag-group。

Native 目录说明：选择或移除一组标签。

## Import

```tsx
import { TagGroup } from "@heroui/react";
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
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `variant` | `"default" \| "surface"` | No | `—` | — |
| `children` | `React.ReactNode` | No | `—` | The children of the component. |
| `className` | `string` | No | `'react-aria-TagGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. |
| `defaultSelectedKeys` | `"all" \| Iterable<Key>` | No | `—` | The initial selected keys in the collection (uncontrolled). |
| `disabledKeys` | `Iterable<Key>` | No | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `disallowEmptySelection` | `boolean` | No | `—` | Whether the collection allows empty selection. |
| `escapeKeyBehavior` | `"none" \| "clearSelection"` | No | `'clearSelection'` | Whether pressing the escape key should clear selection in the TagGroup or not. Most experiences should not modify this option as it eliminates a keyboard user's ability to easily clear selection. Only use if the escape key is being handled externally or should not trigger selection clearing contextually. |
| `onAction` | `(key: Key) => void` | No | `—` | Handler that is called when a user performs an action on an item. The exact user event depends on the collection's `selectionBehavior` prop and the interaction modality. |
| `onRemove` | `(keys: Set<Key>) => void` | No | `—` | Handler that is called when a user deletes a tag. |
| `onSelectionChange` | `(keys: Selection) => void` | No | `—` | Handler that is called when the selection changes. |
| `render` | `DOMRenderFunction<"div", undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKeys` | `"all" \| Iterable<Key>` | No | `—` | The currently selected keys in the collection (controlled). |
| `selectionBehavior` | `SelectionBehavior` | No | `'toggle'` | How multiple selection should behave in the collection. |
| `selectionMode` | `SelectionMode` | No | `—` | The type of selection that is allowed in the collection. |
| `shouldSelectOnPressUp` | `boolean` | No | `—` | Whether selection should occur on press up instead of press down. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `React.CSSProperties` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. |

## Parts

- `TagGroup.List`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open TagGroup in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=14288-4550)

## 画廊

[TagGroup](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/TagGroup)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/tag-group.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import type {Key} from "@heroui/react";

import {Description, Label, Tag, TagGroup} from "@heroui/react";
import {useState} from "react";

export function TagGroupSelectionModes() {
  const [singleSelected, setSingleSelected] = useState<Iterable<Key>>(new Set(["news"]));
  const [multipleSelected, setMultipleSelected] = useState<Iterable<Key>>(
    new Set(["news", "travel"]),
  );

  return (
    <div className="flex flex-col gap-8">
      <TagGroup
        selectedKeys={singleSelected}
        selectionMode="single"
        onSelectionChange={(keys) => setSingleSelected(keys)}
      >
        <Label>Single Selection</Label>
        <TagGroup.List>
          <Tag>News</Tag>
          <Tag>Travel</Tag>
          <Tag>Gaming</Tag>
          <Tag>Shopping</Tag>
        </TagGroup.List>
        <Description>Choose one category</Description>
      </TagGroup>

      <TagGroup
        selectedKeys={multipleSelected}
        selectionMode="multiple"
        onSelectionChange={(keys) => setMultipleSelected(keys)}
      >
        <Label>Multiple Selection</Label>
        <TagGroup.List>
          <Tag>News</Tag>
          <Tag>Travel</Tag>
          <Tag>Gaming</Tag>
          <Tag>Shopping</Tag>
        </TagGroup.List>
        <Description>Choose multiple categories</Description>
      </TagGroup>
    </div>
  );
}

export { TagGroupSelectionModes as Preview };
```
