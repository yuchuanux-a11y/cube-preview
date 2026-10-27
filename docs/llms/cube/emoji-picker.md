# EmojiPicker

Cube component `EmojiPicker` from `@bosagent/cube-ui/emoji-picker`.

Cube component. Source: `packages/cube-ui/src/components/emoji-picker`.

## Import

```tsx
import { EmojiPicker } from "@bosagent/cube-ui/emoji-picker";
import { EmojiPicker } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `size` | `"md" \| "lg" \| "sm"` | No | `"md"` | Size variant controlling trigger, popover, and emoji dimensions. |
| `allowsEmptyCollection` | `boolean` | No | `—` | Whether the select should be allowed to be open when the collection is empty. |
| `autoComplete` | `string` | No | `—` | Describes the type of autocomplete functionality the input should provide if any. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefautocomplete). |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<SelectRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<SelectRenderProps>` | No | `'react-aria-Select'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultOpen` | `boolean` | No | `—` | Sets the default open state of the menu. |
| `defaultSelectedKey` | `Key` | No | `—` | The initial selected key in the collection (uncontrolled). |
| `defaultValue` | `Key \| readonly Key[]` | No | `—` | The default value (uncontrolled). |
| `disabledKeys` | `Iterable<Key>` | No | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `form` | `string` | No | `—` | The `<form>` element to associate the input with. The value of this attribute must be the id of a `<form>` in the same document. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/input#form). |
| `isDisabled` | `boolean` | No | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the input value is invalid. |
| `isOpen` | `boolean` | No | `—` | Sets the open state of the menu. |
| `isRequired` | `boolean` | No | `—` | Whether user input is required on the input before form submission. |
| `name` | `string` | No | `—` | The name of the input, used when submitting an HTML form. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: Key \| Key[]) => void` | No | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is released. |
| `onOpenChange` | `(isOpen: boolean) => void` | No | `—` | Method that is called when the open state of the menu changes. |
| `onSelectionChange` | `(key: Key \| null) => void` | No | `—` | Handler that is called when the selection changes. |
| `placeholder` | `string` | No | `'Select an item' (localized)` | Temporary text that occupies the select when it is empty. |
| `render` | `DOMRenderFunction<"div", SelectRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKey` | `Key` | No | `—` | The currently selected key in the collection (controlled). |
| `selectionMode` | `SelectionMode` | No | `'single'` | Whether single or multiple selection is enabled. |
| `shouldCloseOnSelect` | `boolean` | No | `—` | Whether the Select should close when an item is selected. Defaults to true if selectionMode is single, false otherwise. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<SelectRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: Key \| Key[]) => ValidationError \| true \| null \| undefined` | No | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | No | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `Key \| readonly Key[]` | No | `—` | The current value (controlled). |

## Parts

- `EmojiPicker.Content`
- `EmojiPicker.Footer`
- `EmojiPicker.Grid`
- `EmojiPicker.Item`
- `EmojiPicker.Popover`
- `EmojiPicker.SkinToneContent`
- `EmojiPicker.SkinToneOption`
- `EmojiPicker.SkinTonePicker`
- `EmojiPicker.SkinToneTrigger`
- `EmojiPicker.Trigger`
- `EmojiPicker.Value`

## Example source

```tsx
'use client';

export function Default() {
  return <div className="text-sm">EmojiPicker preview placeholder</div>;
}
```
