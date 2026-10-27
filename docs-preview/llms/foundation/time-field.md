# TimeField

Time input field with labels, descriptions, and validation built on React Aria TimeField

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { TimeField } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | 否 | `—` | — |
| `autoFocus` | `boolean` | 否 | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<DateFieldRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<DateFieldRenderProps>` | 否 | `'react-aria-TimeField'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `T` | 否 | `—` | The default value (uncontrolled). |
| `granularity` | `"hour" \| "minute" \| "second"` | 否 | `'minute'` | Determines the smallest unit that is displayed in the time picker. |
| `hideTimeZone` | `boolean` | 否 | `—` | Whether to hide the time zone abbreviation. |
| `hourCycle` | `24 \| 12` | 否 | `—` | Whether to display the time in 12 or 24 hour format. By default, this is determined by the user's locale. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | 否 | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | 否 | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | 否 | `—` | Whether user input is required on the input before form submission. |
| `maxValue` | `TimeValue` | 否 | `—` | The maximum allowed time that a user may select. |
| `minValue` | `TimeValue` | 否 | `—` | The minimum allowed time that a user may select. |
| `placeholderValue` | `T` | 否 | `—` | A placeholder time that influences the format of the placeholder shown when no value is selected. Defaults to 12:00 AM or 00:00 depending on the hour cycle. |
| `render` | `DOMRenderFunction<"div", DateFieldRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `shouldForceLeadingZeros` | `boolean` | 否 | `—` | Whether to always show leading zeros in the hour field. By default, this is determined by the user's locale. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<DateFieldRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: MappedTimeValue<T>) => ValidationError \| true \| null \| undefined` | 否 | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | 否 | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `T` | 否 | `—` | The current value (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: MappedTimeValue<T>) => void` | 否 | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | 否 | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is released. |

</details>

## Parts

- `TimeField.Group`
- `TimeField.Input`
- `TimeField.InputContainer`
- `TimeField.Prefix`
- `TimeField.Segment`
- `TimeField.Suffix`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-42243
