# NumberStepper

Cube component `NumberStepper` from `@bosagent/cube-ui/number-stepper`.

- 分层：Cube
- 包：`@bosagent/cube-ui/number-stepper`
- 状态：建设中

## Import

```tsx
import { NumberStepper } from "@bosagent/cube-ui/number-stepper";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `formatOptions` | `Format` | 否 | `—` | Formatting options for the value displayed in the number field. This also affects what characters are allowed to be typed by the user. |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | — |
| `autoFocus` | `boolean` | 否 | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<NumberFieldRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<NumberFieldRenderProps>` | 否 | `'react-aria-NumberField'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `commitBehavior` | `"validate" \| "snap"` | 否 | `'snap'` | Controls the behavior of the number field when the user blurs the field after editing. 'snap' will clamp the value to the min/max values, and snap to the nearest step value. 'validate' will not clamp the value, and will validate that the value is within the min/max range and on a valid step. |
| `decrementAriaLabel` | `string` | 否 | `—` | A custom aria-label for the decrement button. If not provided, the localized string "Decrement" is used. |
| `defaultValue` | `number` | 否 | `—` | The default value (uncontrolled). |
| `incrementAriaLabel` | `string` | 否 | `—` | A custom aria-label for the increment button. If not provided, the localized string "Increment" is used. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | 否 | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | 否 | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | 否 | `—` | Whether user input is required on the input before form submission. |
| `isWheelDisabled` | `boolean` | 否 | `—` | Enables or disables changing the value with scroll. |
| `maxValue` | `number` | 否 | `—` | The largest value allowed for the input. |
| `minValue` | `number` | 否 | `—` | The smallest value allowed for the input. |
| `render` | `DOMRenderFunction<"div", NumberFieldRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `step` | `number` | 否 | `—` | The amount that the input value changes with each increment or decrement "tick". |
| `style` | `StyleOrFunction<NumberFieldRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: number) => ValidationError \| true \| null \| undefined` | 否 | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | 否 | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `number` | 否 | `—` | The current value (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: number) => void` | 否 | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | 否 | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is released. |

</details>

## Parts

- `NumberStepper.DecrementButton`
- `NumberStepper.Group`
- `NumberStepper.IncrementButton`
- `NumberStepper.Value`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#NumberStepper
