# SearchField

Search input field with clear button and search icon

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { SearchField } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | 否 | `—` | — |
| `variant` | `"primary" \| "secondary"` | 否 | `—` | — |
| `autoFocus` | `boolean` | 否 | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<SearchFieldRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<SearchFieldRenderProps>` | 否 | `'react-aria-SearchField'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `string` | 否 | `—` | The default value (uncontrolled). |
| `enterKeyHint` | `"search" \| "enter" \| "done" \| "go" \| "next" \| "previous" \| "send"` | 否 | `—` | An enumerated attribute that defines what action label or icon to preset for the enter key on virtual keyboards. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/enterkeyhint). |
| `isDisabled` | `boolean` | 否 | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | 否 | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | 否 | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | 否 | `—` | Whether user input is required on the input before form submission. |
| `render` | `DOMRenderFunction<"div", SearchFieldRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<SearchFieldRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `type` | `"search" \| "text" \| (string & {}) \| "tel" \| "url" \| "email" \| "password"` | 否 | `'search'` | The type of input to render. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdeftype). |
| `validate` | `(value: string) => ValidationError \| true \| null \| undefined` | 否 | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | 否 | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `string` | 否 | `—` | The current value (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `aria-activedescendant` | `string` | 否 | `—` | Identifies the currently active element when DOM focus is on a composite widget, textbox, group, or application. |
| `aria-autocomplete` | `"none" \| "list" \| "both" \| "inline"` | 否 | `—` | Indicates whether inputting text could trigger display of one or more predictions of the user's intended value for an input and specifies how predictions would be presented if they are made. |
| `aria-controls` | `string` | 否 | `—` | Identifies the element (or elements) whose contents or presence are controlled by the current element. |
| `aria-haspopup` | `boolean \| "true" \| "false" \| "dialog" \| "menu" \| "grid" \| "listbox" \| "tree"` | 否 | `—` | Indicates the availability and type of interactive popup element, such as menu or dialog, that can be triggered by an element. |
| `onBlur` | `(e: FocusEvent<HTMLInputElement, Element>) => void` | 否 | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: string) => void` | 否 | `—` | Handler that is called when the value changes. |
| `onClear` | `() => void` | 否 | `—` | Handler that is called when the clear button is pressed. |
| `onFocus` | `(e: FocusEvent<HTMLInputElement, Element>) => void` | 否 | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | 否 | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is released. |
| `onSubmit` | `(value: string) => void` | 否 | `—` | Handler that is called when the SearchField is submitted. |

</details>

## Parts

- `SearchField.ClearButton`
- `SearchField.Group`
- `SearchField.Input`
- `SearchField.SearchIcon`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-34733

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/SearchField
