# Checkbox

Checkboxes allow users to select multiple items from a list of individual items, or to mark one individual item as selected.

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Checkbox } from "@heroui/react";
```

## Figma

[Open Checkbox in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-70992)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `name` | `string` | No | `—` | The name of the checkbox, used when submitting an HTML form. |
| `variant` | `"primary" \| "secondary"` | No | `—` | — |
| `aria-controls` | `string` | No | `—` | Identifies the element (or elements) whose contents or presence are controlled by the current element. |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<CheckboxFieldRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<CheckboxFieldRenderProps>` | No | `'react-aria-CheckboxField'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultSelected` | `boolean` | No | `—` | Whether the element should be selected (uncontrolled). |
| `inputRef` | `React.Ref<HTMLInputElement>` | No | `—` | A ref for the HTML input element. |
| `isDisabled` | `boolean` | No | `—` | Whether the input is disabled. |
| `isIndeterminate` | `boolean` | No | `—` | Indeterminism is presentational only. The indeterminate visual representation remains regardless of user interaction. |
| `isInvalid` | `boolean` | No | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | No | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | No | `—` | Whether user input is required on the input before form submission. |
| `isSelected` | `boolean` | No | `—` | Whether the element should be selected (controlled). |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(isSelected: boolean) => void` | No | `—` | Handler that is called when the element's selection state changes. |
| `onClick` | `(e: MouseEvent<FocusableElement>) => void` | No | `—` | **Not recommended – use `onPress` instead.** `onClick` is an alias for `onPress` provided for compatibility with other libraries. `onPress` provides additional event details for non-mouse interactions. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is released. |
| `onPress` | `(e: PressEvent) => void` | No | `—` | Handler that is called when the press is released over the target. |
| `onPressChange` | `(isPressed: boolean) => void` | No | `—` | Handler that is called when the press state changes. |
| `onPressEnd` | `(e: PressEvent) => void` | No | `—` | Handler that is called when a press interaction ends, either over the target or when the pointer leaves the target. |
| `onPressStart` | `(e: PressEvent) => void` | No | `—` | Handler that is called when a press interaction starts. |
| `onPressUp` | `(e: PressEvent) => void` | No | `—` | Handler that is called when a press is released over the target, regardless of whether it started on the target or not. |
| `render` | `DOMRenderFunction<"div", CheckboxFieldRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<CheckboxFieldRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: boolean) => ValidationError \| true \| null \| undefined` | No | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | No | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `string` | No | `—` | The value of the input element, used when submitting an HTML form. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefvalue). |

## Parts

- `Checkbox.Content`
- `Checkbox.Control`
- `Checkbox.Indicator`

## Example source

```tsx
'use client';

import {Checkbox} from "@heroui/react";

export function Basic() {
  return (
    <Checkbox name="basic-terms">
      <Checkbox.Content>
        <Checkbox.Control>
          <Checkbox.Indicator />
        </Checkbox.Control>
        Accept terms and conditions
      </Checkbox.Content>
    </Checkbox>
  );
}

export { Basic as Preview };
```
