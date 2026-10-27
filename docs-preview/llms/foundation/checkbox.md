# Checkbox

Checkboxes allow users to select multiple items from a list of individual items, or to mark one individual item as selected.

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { Checkbox } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `name` | `string` | 否 | `—` | The name of the checkbox, used when submitting an HTML form. |
| `variant` | `"primary" \| "secondary"` | 否 | `—` | — |
| `autoFocus` | `boolean` | 否 | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<CheckboxFieldRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<CheckboxFieldRenderProps>` | 否 | `'react-aria-CheckboxField'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultSelected` | `boolean` | 否 | `—` | Whether the element should be selected (uncontrolled). |
| `inputRef` | `React.Ref<HTMLInputElement>` | 否 | `—` | A ref for the HTML input element. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the input is disabled. |
| `isIndeterminate` | `boolean` | 否 | `—` | Indeterminism is presentational only. The indeterminate visual representation remains regardless of user interaction. |
| `isInvalid` | `boolean` | 否 | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | 否 | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | 否 | `—` | Whether user input is required on the input before form submission. |
| `isSelected` | `boolean` | 否 | `—` | Whether the element should be selected (controlled). |
| `render` | `DOMRenderFunction<"div", CheckboxFieldRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<CheckboxFieldRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: boolean) => ValidationError \| true \| null \| undefined` | 否 | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | 否 | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `string` | 否 | `—` | The value of the input element, used when submitting an HTML form. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefvalue). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `aria-controls` | `string` | 否 | `—` | Identifies the element (or elements) whose contents or presence are controlled by the current element. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(isSelected: boolean) => void` | 否 | `—` | Handler that is called when the element's selection state changes. |
| `onClick` | `(e: MouseEvent<FocusableElement>) => void` | 否 | `—` | **Not recommended – use `onPress` instead.** `onClick` is an alias for `onPress` provided for compatibility with other libraries. `onPress` provides additional event details for non-mouse interactions. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | 否 | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is released. |
| `onPress` | `(e: PressEvent) => void` | 否 | `—` | Handler that is called when the press is released over the target. |
| `onPressChange` | `(isPressed: boolean) => void` | 否 | `—` | Handler that is called when the press state changes. |
| `onPressEnd` | `(e: PressEvent) => void` | 否 | `—` | Handler that is called when a press interaction ends, either over the target or when the pointer leaves the target. |
| `onPressStart` | `(e: PressEvent) => void` | 否 | `—` | Handler that is called when a press interaction starts. |
| `onPressUp` | `(e: PressEvent) => void` | 否 | `—` | Handler that is called when a press is released over the target, regardless of whether it started on the target or not. |

</details>

## Parts

- `Checkbox.Content`
- `Checkbox.Control`
- `Checkbox.Indicator`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-70992

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Checkbox
