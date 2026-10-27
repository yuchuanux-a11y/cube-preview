# ListBox

A listbox displays a list of options and allows a user to select one or more of them

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { ListBox } from "@heroui/react";
```

## Figma

[Open ListBox in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-70869)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `className` | `string` | No | `'react-aria-ListBox'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `variant` | `"default" \| "danger"` | No | `—` | — |
| `autoFocus` | `boolean \| FocusStrategy` | No | `—` | Whether to auto focus the listbox or an option. |
| `children` | `React.ReactNode \| ((item: T) => ReactNode)` | No | `—` | The contents of the collection. |
| `defaultSelectedKeys` | `"all" \| Iterable<Key>` | No | `—` | The initial selected keys in the collection (uncontrolled). |
| `dependencies` | `readonly any[]` | No | `—` | Values that should invalidate the item cache when using dynamic collections. |
| `disabledKeys` | `Iterable<Key>` | No | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `disallowEmptySelection` | `boolean` | No | `—` | Whether the collection allows empty selection. |
| `dragAndDropHooks` | `DragAndDropHooks<NoInfer<T>>` | No | `—` | The drag and drop hooks returned by `useDragAndDrop` used to enable drag and drop behavior for the ListBox. |
| `escapeKeyBehavior` | `"none" \| "clearSelection"` | No | `'clearSelection'` | Whether pressing the escape key should clear selection in the listbox or not. Most experiences should not modify this option as it eliminates a keyboard user's ability to easily clear selection. Only use if the escape key is being handled externally or should not trigger selection clearing contextually. |
| `items` | `Iterable<T>` | No | `—` | Item objects in the collection. |
| `layout` | `"grid" \| "stack"` | No | `'stack'` | Whether the items are arranged in a stack or grid. |
| `onAction` | `(key: Key) => void` | No | `—` | Handler that is called when a user performs an action on an item. The exact user event depends on the collection's `selectionBehavior` prop and the interaction modality. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `onSelectionChange` | `(keys: Selection) => void` | No | `—` | Handler that is called when the selection changes. |
| `orientation` | `Orientation` | No | `'vertical'` | The primary orientation of the items. Usually this is the direction that the collection scrolls. |
| `render` | `DOMRenderFunction<"div", ListBoxRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `renderEmptyState` | `(props: ListBoxRenderProps) => ReactNode` | No | `—` | Provides content to display when there are no items in the list. |
| `selectedKeys` | `"all" \| Iterable<Key>` | No | `—` | The currently selected keys in the collection (controlled). |
| `selectionBehavior` | `SelectionBehavior` | No | `'toggle'` | How multiple selection should behave in the collection. |
| `selectionMode` | `SelectionMode` | No | `—` | The type of selection that is allowed in the collection. |
| `shouldFocusOnHover` | `boolean` | No | `—` | Whether options should be focused when the user hovers over them. |
| `shouldFocusWrap` | `boolean` | No | `—` | Whether focus should wrap around when the end/start is reached. |
| `shouldSelectOnPressUp` | `boolean` | No | `—` | Whether selection should occur on press up instead of press down. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ListBoxRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `ListBox.Item`
- `ListBox.ItemIndicator`
- `ListBox.Section`

## Example source

```tsx
'use client';

import {Avatar, Description, Label, ListBox} from "@heroui/react";

export function Default() {
  return (
    <ListBox aria-label="Users" className="w-[220px]" selectionMode="single">
      <ListBox.Item id="1" textValue="Bob">
        <Avatar size="sm">
          <Avatar.Image
            alt="Bob"
            src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/blue.jpg"
          />
          <Avatar.Fallback>B</Avatar.Fallback>
        </Avatar>
        <div className="flex flex-col">
          <Label>Bob</Label>
          <Description>bob@heroui.com</Description>
        </div>
        <ListBox.ItemIndicator />
      </ListBox.Item>
      <ListBox.Item id="2" textValue="Fred">
        <Avatar size="sm">
          <Avatar.Image
            alt="Fred"
            src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/green.jpg"
          />
          <Avatar.Fallback>F</Avatar.Fallback>
        </Avatar>
        <div className="flex flex-col">
          <Label>Fred</Label>
          <Description>fred@heroui.com</Description>
        </div>
        <ListBox.ItemIndicator />
      </ListBox.Item>
      <ListBox.Item id="3" textValue="Martha">
        <Avatar size="sm">
          <Avatar.Image
            alt="Martha"
            src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/purple.jpg"
          />
          <Avatar.Fallback>M</Avatar.Fallback>
        </Avatar>
        <div className="flex flex-col">
          <Label>Martha</Label>
          <Description>martha@heroui.com</Description>
        </div>
        <ListBox.ItemIndicator />
      </ListBox.Item>
    </ListBox>
  );
}

export { Default as Preview };
```
