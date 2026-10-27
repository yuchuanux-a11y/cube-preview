# DateRangePicker

Composable date range picker built on React Aria DateRangePicker with DateField and RangeCalendar composition

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { DateRangePicker } from "@heroui/react";
```

## Figma

[Open DateRangePicker in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17295-58175)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `allowsNonContiguousRanges` | `boolean` | No | `—` | When combined with `isDateUnavailable`, determines whether non-contiguous ranges, i.e. ranges containing unavailable dates, may be selected. |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<DateRangePickerRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<DateRangePickerRenderProps>` | No | `'react-aria-DateRangePicker'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultOpen` | `boolean` | No | `—` | Whether the overlay is open by default (uncontrolled). |
| `defaultValue` | `RangeValue<T>` | No | `—` | The default value (uncontrolled). |
| `endName` | `string` | No | `—` | The name of the end date input element, used when submitting an HTML form. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefname). |
| `firstDayOfWeek` | `"sun" \| "mon" \| "tue" \| "wed" \| "thu" \| "fri" \| "sat"` | No | `—` | The day that starts the week. |
| `granularity` | `Granularity` | No | `—` | Determines the smallest unit that is displayed in the date picker. By default, this is `"day"` for dates, and `"minute"` for times. |
| `hideTimeZone` | `boolean` | No | `false` | Whether to hide the time zone abbreviation. |
| `hourCycle` | `24 \| 12` | No | `—` | Whether to display the time in 12 or 24 hour format. By default, this is determined by the user's locale. |
| `isDateUnavailable` | `(date: DateValue, anchorDate: CalendarDate \| null) => boolean` | No | `—` | Callback that is called for each date of the calendar. If it returns true, then the date is unavailable. |
| `isDisabled` | `boolean` | No | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the input value is invalid. |
| `isOpen` | `boolean` | No | `—` | Whether the overlay is open by default (controlled). |
| `isReadOnly` | `boolean` | No | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | No | `—` | Whether user input is required on the input before form submission. |
| `maxValue` | `DateValue` | No | `—` | The maximum allowed date that a user may select. |
| `minValue` | `DateValue` | No | `—` | The minimum allowed date that a user may select. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: RangeValue<MappedDateValue<T>>) => void` | No | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is released. |
| `onOpenChange` | `(isOpen: boolean) => void` | No | `—` | Handler that is called when the overlay's open state changes. |
| `pageBehavior` | `PageBehavior` | No | `visible` | Controls the behavior of paging. Pagination either works by advancing the visible page by visibleDuration (default) or one unit of visibleDuration. |
| `placeholderValue` | `T` | No | `—` | A placeholder date that influences the format of the placeholder shown when no value is selected. Defaults to today's date at midnight. |
| `render` | `DOMRenderFunction<"div", DateRangePickerRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `shouldCloseOnSelect` | `boolean \| (() => boolean)` | No | `true` | Determines whether the date picker popover should close automatically when a date is selected. |
| `shouldForceLeadingZeros` | `boolean` | No | `—` | Whether to always show leading zeros in the month, day, and hour fields. By default, this is determined by the user's locale. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `startName` | `string` | No | `—` | The name of the start date input element, used when submitting an HTML form. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefname). |
| `style` | `StyleOrFunction<DateRangePickerRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: RangeValue<MappedDateValue<T>>) => ValidationError \| true \| null \| undefined` | No | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | No | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `RangeValue<T>` | No | `—` | The current value (controlled). |

## Parts

- `DateRangePicker.Popover`
- `DateRangePicker.RangeSeparator`
- `DateRangePicker.Trigger`
- `DateRangePicker.TriggerIndicator`

## Example source

```tsx
'use client';

import {DateField, DateRangePicker, Label, RangeCalendar} from "@heroui/react";

export function Basic() {
  return (
    <DateRangePicker className="w-80" endName="endDate" startName="startDate">
      <Label>Trip dates</Label>
      <DateField.Group fullWidth>
        <DateField.Input slot="start">
          {(segment) => <DateField.Segment segment={segment} />}
        </DateField.Input>
        <DateRangePicker.RangeSeparator />
        <DateField.Input slot="end">
          {(segment) => <DateField.Segment segment={segment} />}
        </DateField.Input>
        <DateField.Suffix>
          <DateRangePicker.Trigger>
            <DateRangePicker.TriggerIndicator />
          </DateRangePicker.Trigger>
        </DateField.Suffix>
      </DateField.Group>
      <DateRangePicker.Popover>
        <RangeCalendar aria-label="Trip dates">
          <RangeCalendar.Header>
            <RangeCalendar.YearPickerTrigger>
              <RangeCalendar.YearPickerTriggerHeading />
              <RangeCalendar.YearPickerTriggerIndicator />
            </RangeCalendar.YearPickerTrigger>
            <RangeCalendar.NavButton slot="previous" />
            <RangeCalendar.NavButton slot="next" />
          </RangeCalendar.Header>
          <RangeCalendar.Grid>
            <RangeCalendar.GridHeader>
              {(day) => <RangeCalendar.HeaderCell>{day}</RangeCalendar.HeaderCell>}
            </RangeCalendar.GridHeader>
            <RangeCalendar.GridBody>
              {(date) => <RangeCalendar.Cell date={date} />}
            </RangeCalendar.GridBody>
          </RangeCalendar.Grid>
          <RangeCalendar.YearPickerGrid>
            <RangeCalendar.YearPickerGridBody>
              {({year}) => <RangeCalendar.YearPickerCell year={year} />}
            </RangeCalendar.YearPickerGridBody>
          </RangeCalendar.YearPickerGrid>
        </RangeCalendar>
      </DateRangePicker.Popover>
    </DateRangePicker>
  );
}

export { Basic as Preview };
```
