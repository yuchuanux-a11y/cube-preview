# CellSelect

Cube component `CellSelect` from `@bosagent/cube-ui/cell-select`.

- 分层：Cube
- 包：`@bosagent/cube-ui/cell-select`
- 状态：建设中

## Import

```tsx
import { CellSelect } from "@bosagent/cube-ui/cell-select";
import { CellSelect } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | 否 | `—` | — |
| `items` | `Iterable<T, M>` | 否 | `—` | — |
| `variant` | `"default" \| "secondary"` | 否 | `"default"` | Visual variant. |
| `allowsEmptyCollection` | `boolean` | 否 | `—` | Whether the select should be allowed to be open when the collection is empty. |
| `autoComplete` | `string` | 否 | `—` | Describes the type of autocomplete functionality the input should provide if any. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefautocomplete). |
| `autoFocus` | `boolean` | 否 | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<SelectRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<SelectRenderProps>` | 否 | `'react-aria-Select'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultOpen` | `boolean` | 否 | `—` | Sets the default open state of the menu. |
| `defaultSelectedKey` | `Key` | 否 | `—` | The initial selected key in the collection (uncontrolled). |
| `defaultValue` | `ValueType<M>` | 否 | `—` | The default value (uncontrolled). |
| `disabledKeys` | `Iterable<Key>` | 否 | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `form` | `string` | 否 | `—` | The `<form>` element to associate the input with. The value of this attribute must be the id of a `<form>` in the same document. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/input#form). |
| `isDisabled` | `boolean` | 否 | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | 否 | `—` | Whether the input value is invalid. |
| `isOpen` | `boolean` | 否 | `—` | Sets the open state of the menu. |
| `isRequired` | `boolean` | 否 | `—` | Whether user input is required on the input before form submission. |
| `name` | `string` | 否 | `—` | The name of the input, used when submitting an HTML form. |
| `placeholder` | `string` | 否 | `'Select an item' (localized)` | Temporary text that occupies the select when it is empty. |
| `render` | `DOMRenderFunction<"div", SelectRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKey` | `Key` | 否 | `—` | The currently selected key in the collection (controlled). |
| `selectionMode` | `M` | 否 | `'single'` | Whether single or multiple selection is enabled. |
| `shouldCloseOnSelect` | `boolean` | 否 | `—` | Whether the Select should close when an item is selected. Defaults to true if selectionMode is single, false otherwise. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<SelectRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: ValidationType<M>) => ValidationError \| true \| null \| undefined` | 否 | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | 否 | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `ValueType<M>` | 否 | `—` | The current value (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onClear` | `() => void` | 否 | `—` | Handler that is called when the selection is cleared. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: ChangeValueType<M>) => void` | 否 | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | 否 | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is released. |
| `onOpenChange` | `(isOpen: boolean) => void` | 否 | `—` | Method that is called when the open state of the menu changes. |
| `onSelectionChange` | `(key: Key \| null) => void` | 否 | `—` | Handler that is called when the selection changes. |

</details>

## Parts

- `CellSelect.Indicator`
- `CellSelect.Label`
- `CellSelect.Popover`
- `CellSelect.Trigger`
- `CellSelect.Value`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#CellSelect
