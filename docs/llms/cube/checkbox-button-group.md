# CheckboxButtonGroup

Cube component `CheckboxButtonGroup` from `@bosagent/cube-ui/checkbox-button-group`.

Cube component. Source: `packages/cube-ui/src/components/checkbox-button-group`.

## Import

```tsx
import { CheckboxButtonGroup } from "@bosagent/cube-ui/checkbox-button-group";
import { CheckboxButtonGroup } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `layout` | `"grid" \| "flex"` | No | `"flex"` | Layout mode for items. |
| `variant` | `"primary" \| "secondary"` | No | `—` | — |
| `children` | `ChildrenOrFunction<CheckboxGroupRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<CheckboxGroupRenderProps>` | No | `'react-aria-CheckboxGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `string[]` | No | `—` | The default value (uncontrolled). |
| `isDisabled` | `boolean` | No | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | No | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | No | `—` | Whether user input is required on the input before form submission. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: string[]) => void` | No | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `render` | `DOMRenderFunction<"div", CheckboxGroupRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<CheckboxGroupRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: string[]) => ValidationError \| true \| null \| undefined` | No | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | No | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `string[]` | No | `—` | The current value (controlled). |

## Parts

- `CheckboxButtonGroup.Indicator`
- `CheckboxButtonGroup.Item`
- `CheckboxButtonGroup.ItemContent`
- `CheckboxButtonGroup.ItemIcon`

## Example source

```tsx
'use client';

import { CheckboxButtonGroup } from '@components/checkbox-button-group';
import { Description, Label } from '@heroui/react';

const features = [
  {
    description: 'Real-time threat detection and prevention',
    value: 'security',
  },
  {
    description: 'Cloud-based storage with automatic backups',
    value: 'storage',
  },
  {
    description: 'Usage reports and performance dashboards',
    value: 'analytics',
  },
];

export function Default() {
  return (
    <CheckboxButtonGroup
      className="w-[360px]"
      defaultValue={['security', 'storage']}
      name="features"
      variant="secondary"
    >
      <Label>Select features</Label>
      <Description>Choose all that apply to your project</Description>
      {features.map((feature) => (
        <CheckboxButtonGroup.Item key={feature.value} value={feature.value}>
          <CheckboxButtonGroup.Indicator />
          <CheckboxButtonGroup.ItemContent>
            <Label className="capitalize">{feature.value}</Label>
            <Description>{feature.description}</Description>
          </CheckboxButtonGroup.ItemContent>
        </CheckboxButtonGroup.Item>
      ))}
    </CheckboxButtonGroup>
  );
}
```
