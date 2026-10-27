# NumberStepper

Cube component `NumberStepper` from `@bosagent/cube-ui/number-stepper`.

Cube component. Source: `packages/cube-ui/src/components/number-stepper`.

## Import

```tsx
import { NumberStepper } from "@bosagent/cube-ui/number-stepper";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `formatOptions` | `Format` | No | `—` | Formatting options for the value displayed in the number field. This also affects what characters are allowed to be typed by the user. |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<NumberFieldRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<NumberFieldRenderProps>` | No | `'react-aria-NumberField'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `commitBehavior` | `"validate" \| "snap"` | No | `'snap'` | Controls the behavior of the number field when the user blurs the field after editing. 'snap' will clamp the value to the min/max values, and snap to the nearest step value. 'validate' will not clamp the value, and will validate that the value is within the min/max range and on a valid step. |
| `decrementAriaLabel` | `string` | No | `—` | A custom aria-label for the decrement button. If not provided, the localized string "Decrement" is used. |
| `defaultValue` | `number` | No | `—` | The default value (uncontrolled). |
| `incrementAriaLabel` | `string` | No | `—` | A custom aria-label for the increment button. If not provided, the localized string "Increment" is used. |
| `isDisabled` | `boolean` | No | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | No | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | No | `—` | Whether user input is required on the input before form submission. |
| `isWheelDisabled` | `boolean` | No | `—` | Enables or disables changing the value with scroll. |
| `maxValue` | `number` | No | `—` | The largest value allowed for the input. |
| `minValue` | `number` | No | `—` | The smallest value allowed for the input. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: number) => void` | No | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is released. |
| `render` | `DOMRenderFunction<"div", NumberFieldRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `step` | `number` | No | `—` | The amount that the input value changes with each increment or decrement "tick". |
| `style` | `StyleOrFunction<NumberFieldRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: number) => ValidationError \| true \| null \| undefined` | No | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | No | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `number` | No | `—` | The current value (controlled). |

## Parts

- `NumberStepper.DecrementButton`
- `NumberStepper.Group`
- `NumberStepper.IncrementButton`
- `NumberStepper.Value`

## Example source

```tsx
'use client';

import { NumberStepper } from '@components/number-stepper';

export function Default() {
  return (
    <NumberStepper
      aria-label="Quantity"
      defaultValue={1}
      maxValue={99}
      minValue={0}
    >
      <NumberStepper.Group>
        <NumberStepper.DecrementButton />
        <NumberStepper.Value />
        <NumberStepper.IncrementButton />
      </NumberStepper.Group>
    </NumberStepper>
  );
}
```
