# ComboBox

A combo box combines a text input with a listbox, allowing users to filter a list of options to items matching a query

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { ComboBox } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | 否 | `—` | — |
| `items` | `Iterable<T>` | 否 | `—` | The list of ComboBox items (controlled). |
| `variant` | `"primary" \| "secondary"` | 否 | `"primary"` | The variant of the combo box. |
| `allowsCustomValue` | `boolean` | 否 | `—` | Whether the ComboBox allows a non-item matching input value to be set. |
| `allowsEmptyCollection` | `boolean` | 否 | `—` | Whether the combo box allows the menu to be open when the collection is empty. |
| `autoFocus` | `boolean` | 否 | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<ComboBoxRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ComboBoxRenderProps>` | 否 | `'react-aria-ComboBox'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultFilter` | `(textValue: string, inputValue: string) => boolean` | 否 | `—` | The filter function used to determine if an option should be included in the combo box list. By default, a language-sensitive "contains" filter from `useFilter` is used. |
| `defaultInputValue` | `string` | 否 | `—` | The default value of the ComboBox input (uncontrolled). |
| `defaultItems` | `Iterable<T>` | 否 | `—` | The list of ComboBox items (uncontrolled). |
| `defaultSelectedKey` | `Key` | 否 | `—` | The initial selected key in the collection (uncontrolled). |
| `defaultValue` | `ValueType<M>` | 否 | `—` | The default value (uncontrolled). |
| `disabledKeys` | `Iterable<Key>` | 否 | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `formValue` | `"key" \| "text"` | 否 | `'key'` | Whether the text or key of the selected item is submitted as part of an HTML form. When `allowsCustomValue` is `true`, this option does not apply and the text is always submitted. |
| `inputValue` | `string` | 否 | `—` | The value of the ComboBox input (controlled). |
| `isDisabled` | `boolean` | 否 | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | 否 | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | 否 | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | 否 | `—` | Whether user input is required on the input before form submission. |
| `menuTrigger` | `MenuTriggerAction` | 否 | `'input'` | The interaction required to display the ComboBox menu. |
| `render` | `DOMRenderFunction<"div", ComboBoxRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKey` | `Key` | 否 | `—` | The currently selected key in the collection (controlled). |
| `selectionMode` | `M` | 否 | `'single'` | Whether single or multiple selection is enabled. |
| `shouldFocusWrap` | `boolean` | 否 | `—` | Whether keyboard navigation is circular. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ComboBoxRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: ComboBoxValidationValue<M>) => ValidationError \| true \| null \| undefined` | 否 | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | 否 | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `ValueType<M>` | 否 | `—` | The current value (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onBlur` | `(e: FocusEvent<HTMLInputElement, Element>) => void` | 否 | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: ChangeValueType<M>) => void` | 否 | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<HTMLInputElement, Element>) => void` | 否 | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | 否 | `—` | Handler that is called when the element's focus status changes. |
| `onInputChange` | `(value: string) => void` | 否 | `—` | Handler that is called when the ComboBox input value changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is released. |
| `onOpenChange` | `(isOpen: boolean, menuTrigger?: MenuTriggerAction) => void` | 否 | `—` | Method that is called when the open state of the menu changes. Returns the new open state and the action that caused the opening of the menu. |
| `onSelectionChange` | `(key: Key \| null) => void` | 否 | `—` | Handler that is called when the selection changes. |

</details>

## Parts

- `ComboBox.InputGroup`
- `ComboBox.Popover`
- `ComboBox.Trigger`
- `ComboBox.Value`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=14118-33084
