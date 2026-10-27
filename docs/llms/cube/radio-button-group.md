# RadioButtonGroup

Cube component `RadioButtonGroup` from `@bosagent/cube-ui/radio-button-group`.

Cube component. Source: `packages/cube-ui/src/components/radio-button-group`.

## Import

```tsx
import { RadioButtonGroup } from "@bosagent/cube-ui/radio-button-group";
import { RadioButtonGroup } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `layout` | `"grid" \| "flex"` | No | `"flex"` | Layout mode for items. |
| `variant` | `"primary" \| "secondary"` | No | `—` | — |
| `children` | `ChildrenOrFunction<RadioGroupRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<RadioGroupRenderProps>` | No | `'react-aria-RadioGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `string` | No | `—` | The default value (uncontrolled). |
| `isDisabled` | `boolean` | No | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | No | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | No | `—` | Whether user input is required on the input before form submission. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: string) => void` | No | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `orientation` | `Orientation` | No | `'vertical'` | The axis the Radio Button(s) should align with. |
| `render` | `DOMRenderFunction<"div", RadioGroupRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<RadioGroupRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: string) => ValidationError \| true \| null \| undefined` | No | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | No | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `string` | No | `—` | The current value (controlled). |

## Parts

- `RadioButtonGroup.Indicator`
- `RadioButtonGroup.Item`
- `RadioButtonGroup.ItemContent`
- `RadioButtonGroup.ItemIcon`

## Example source

```tsx
'use client';

import { NumberValue } from '@components/number-value';
import { RadioButtonGroup } from '@components/radio-button-group';
import { Description, Label } from '@heroui/react';

const plans = [
  {
    description: 'For individuals and small projects',
    price: 5,
    value: 'starter',
  },
  { description: 'For growing teams and businesses', price: 15, value: 'pro' },
  {
    description: 'For large organizations at scale',
    price: 45,
    value: 'enterprise',
  },
];

export function Default() {
  return (
    <RadioButtonGroup
      className="w-[min(360px,calc(100vw-2rem))]"
      defaultValue="pro"
      name="plan"
      variant="secondary"
    >
      <Label>Select a plan</Label>
      <Description>Choose the plan that suits your needs</Description>
      {plans.map((plan) => (
        <RadioButtonGroup.Item key={plan.value} value={plan.value}>
          <RadioButtonGroup.Indicator />
          <RadioButtonGroup.ItemContent>
            <Label className="capitalize">{plan.value}</Label>
            <Description>{plan.description}</Description>
            <NumberValue
              className="mt-2 text-sm font-semibold"
              currency="USD"
              maximumFractionDigits={0}
              style="currency"
              value={plan.price}
            >
              <NumberValue.Suffix>
                <span className="text-xs font-normal text-muted">/mo</span>
              </NumberValue.Suffix>
            </NumberValue>
          </RadioButtonGroup.ItemContent>
        </RadioButtonGroup.Item>
      ))}
    </RadioButtonGroup>
  );
}
```
