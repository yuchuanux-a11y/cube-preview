# ComboBox

A combo box combines a text input with a listbox, allowing users to filter a list of options to items matching a query

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { ComboBox } from "@heroui/react";
```

## Figma

[Open ComboBox in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=14118-33084)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | No | `—` | — |
| `items` | `Iterable<T>` | No | `—` | The list of ComboBox items (controlled). |
| `variant` | `"primary" \| "secondary"` | No | `"primary"` | The variant of the combo box. |
| `allowsCustomValue` | `boolean` | No | `—` | Whether the ComboBox allows a non-item matching input value to be set. |
| `allowsEmptyCollection` | `boolean` | No | `—` | Whether the combo box allows the menu to be open when the collection is empty. |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<ComboBoxRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ComboBoxRenderProps>` | No | `'react-aria-ComboBox'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultFilter` | `(textValue: string, inputValue: string) => boolean` | No | `—` | The filter function used to determine if an option should be included in the combo box list. By default, a language-sensitive "contains" filter from `useFilter` is used. |
| `defaultInputValue` | `string` | No | `—` | The default value of the ComboBox input (uncontrolled). |
| `defaultItems` | `Iterable<T>` | No | `—` | The list of ComboBox items (uncontrolled). |
| `defaultSelectedKey` | `Key` | No | `—` | The initial selected key in the collection (uncontrolled). |
| `defaultValue` | `ValueType<M>` | No | `—` | The default value (uncontrolled). |
| `disabledKeys` | `Iterable<Key>` | No | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `formValue` | `"key" \| "text"` | No | `'key'` | Whether the text or key of the selected item is submitted as part of an HTML form. When `allowsCustomValue` is `true`, this option does not apply and the text is always submitted. |
| `inputValue` | `string` | No | `—` | The value of the ComboBox input (controlled). |
| `isDisabled` | `boolean` | No | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | No | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | No | `—` | Whether user input is required on the input before form submission. |
| `menuTrigger` | `MenuTriggerAction` | No | `'input'` | The interaction required to display the ComboBox menu. |
| `onBlur` | `(e: FocusEvent<HTMLInputElement, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: ChangeValueType<M>) => void` | No | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<HTMLInputElement, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `onInputChange` | `(value: string) => void` | No | `—` | Handler that is called when the ComboBox input value changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is released. |
| `onOpenChange` | `(isOpen: boolean, menuTrigger?: MenuTriggerAction) => void` | No | `—` | Method that is called when the open state of the menu changes. Returns the new open state and the action that caused the opening of the menu. |
| `onSelectionChange` | `(key: Key \| null) => void` | No | `—` | Handler that is called when the selection changes. |
| `render` | `DOMRenderFunction<"div", ComboBoxRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKey` | `Key` | No | `—` | The currently selected key in the collection (controlled). |
| `selectionMode` | `M` | No | `'single'` | Whether single or multiple selection is enabled. |
| `shouldFocusWrap` | `boolean` | No | `—` | Whether keyboard navigation is circular. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ComboBoxRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: ComboBoxValidationValue<M>) => ValidationError \| true \| null \| undefined` | No | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | No | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `ValueType<M>` | No | `—` | The current value (controlled). |

## Parts

- `ComboBox.InputGroup`
- `ComboBox.Popover`
- `ComboBox.Trigger`
- `ComboBox.Value`

## Example source

```tsx
'use client';

import {ComboBox, Input, Label, ListBox} from "@heroui/react";

export function Default() {
  return (
    <ComboBox className="w-[256px]">
      <Label>Favorite Animal</Label>
      <ComboBox.InputGroup>
        <Input placeholder="Search animals..." />
        <ComboBox.Trigger />
      </ComboBox.InputGroup>
      <ComboBox.Popover>
        <ListBox>
          <ListBox.Item id="aardvark" textValue="Aardvark">
            Aardvark
            <ListBox.ItemIndicator />
          </ListBox.Item>
          <ListBox.Item id="cat" textValue="Cat">
            Cat
            <ListBox.ItemIndicator />
          </ListBox.Item>
          <ListBox.Item id="dog" textValue="Dog">
            Dog
            <ListBox.ItemIndicator />
          </ListBox.Item>
          <ListBox.Item id="kangaroo" textValue="Kangaroo">
            Kangaroo
            <ListBox.ItemIndicator />
          </ListBox.Item>
          <ListBox.Item id="panda" textValue="Panda">
            Panda
            <ListBox.ItemIndicator />
          </ListBox.Item>
          <ListBox.Item id="snake" textValue="Snake">
            Snake
            <ListBox.ItemIndicator />
          </ListBox.Item>
        </ListBox>
      </ComboBox.Popover>
    </ComboBox>
  );
}

export { Default as Preview };
```
