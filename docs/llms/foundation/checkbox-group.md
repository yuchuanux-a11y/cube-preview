# CheckboxGroup

A checkbox group component for managing multiple checkbox selections

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { CheckboxGroup } from "@heroui/react";
```

## Figma

[Open CheckboxGroup in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17290-24388)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
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

## Example source

```tsx
'use client';

import {Checkbox, CheckboxGroup, Description, Label} from "@heroui/react";

export function Basic() {
  return (
    <CheckboxGroup name="interests">
      <Label>Select your interests</Label>
      <Description>Choose all that apply</Description>
      <Checkbox value="coding">
        <Checkbox.Content>
          <Checkbox.Control>
            <Checkbox.Indicator />
          </Checkbox.Control>
          Coding
        </Checkbox.Content>
        <Description>Love building software</Description>
      </Checkbox>
      <Checkbox value="design">
        <Checkbox.Content>
          <Checkbox.Control>
            <Checkbox.Indicator />
          </Checkbox.Control>
          Design
        </Checkbox.Content>
        <Description>Enjoy creating beautiful interfaces</Description>
      </Checkbox>
      <Checkbox value="writing">
        <Checkbox.Content>
          <Checkbox.Control>
            <Checkbox.Indicator />
          </Checkbox.Control>
          Writing
        </Checkbox.Content>
        <Description>Passionate about content creation</Description>
      </Checkbox>
    </CheckboxGroup>
  );
}

export { Basic as Preview };
```
