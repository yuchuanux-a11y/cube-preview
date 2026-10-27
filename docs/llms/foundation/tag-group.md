# TagGroup

A focusable list of tags with support for keyboard navigation, selection, and removal

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { TagGroup } from "@heroui/react";
```

## Figma

[Open TagGroup in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=14288-4550)

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
