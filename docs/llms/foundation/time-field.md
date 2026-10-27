# TimeField

Time input field with labels, descriptions, and validation built on React Aria TimeField

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { TimeField } from "@heroui/react";
```

## Figma

[Open TimeField in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-42243)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | No | `—` | — |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<DateFieldRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<DateFieldRenderProps>` | No | `'react-aria-TimeField'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `T` | No | `—` | The default value (uncontrolled). |
| `granularity` | `"hour" \| "minute" \| "second"` | No | `'minute'` | Determines the smallest unit that is displayed in the time picker. |
| `hideTimeZone` | `boolean` | No | `—` | Whether to hide the time zone abbreviation. |
| `hourCycle` | `24 \| 12` | No | `—` | Whether to display the time in 12 or 24 hour format. By default, this is determined by the user's locale. |
| `isDisabled` | `boolean` | No | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | No | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | No | `—` | Whether user input is required on the input before form submission. |
| `maxValue` | `TimeValue` | No | `—` | The maximum allowed time that a user may select. |
| `minValue` | `TimeValue` | No | `—` | The minimum allowed time that a user may select. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: MappedTimeValue<T>) => void` | No | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is released. |
| `placeholderValue` | `T` | No | `—` | A placeholder time that influences the format of the placeholder shown when no value is selected. Defaults to 12:00 AM or 00:00 depending on the hour cycle. |
| `render` | `DOMRenderFunction<"div", DateFieldRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `shouldForceLeadingZeros` | `boolean` | No | `—` | Whether to always show leading zeros in the hour field. By default, this is determined by the user's locale. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<DateFieldRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: MappedTimeValue<T>) => ValidationError \| true \| null \| undefined` | No | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | No | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `T` | No | `—` | The current value (controlled). |

## Parts

- `TimeField.Group`
- `TimeField.Input`
- `TimeField.InputContainer`
- `TimeField.Prefix`
- `TimeField.Segment`
- `TimeField.Suffix`

## Example source

```tsx
'use client';

import {Label, TimeField} from "@heroui/react";

export function Basic() {
  return (
    <TimeField className="w-[256px]" name="time">
      <Label>Time</Label>
      <TimeField.Group>
        <TimeField.Input>{(segment) => <TimeField.Segment segment={segment} />}</TimeField.Input>
      </TimeField.Group>
    </TimeField>
  );
}

export { Basic as Preview };
```
