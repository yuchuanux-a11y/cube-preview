# DateRangePicker

Composable date range picker built on React Aria DateRangePicker with DateField and RangeCalendar composition

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { DateRangePicker } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `allowsNonContiguousRanges` | `boolean` | 否 | `—` | When combined with `isDateUnavailable`, determines whether non-contiguous ranges, i.e. ranges containing unavailable dates, may be selected. |
| `autoFocus` | `boolean` | 否 | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<DateRangePickerRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<DateRangePickerRenderProps>` | 否 | `'react-aria-DateRangePicker'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultOpen` | `boolean` | 否 | `—` | Whether the overlay is open by default (uncontrolled). |
| `defaultValue` | `RangeValue<T>` | 否 | `—` | The default value (uncontrolled). |
| `endName` | `string` | 否 | `—` | The name of the end date input element, used when submitting an HTML form. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefname). |
| `firstDayOfWeek` | `"sun" \| "mon" \| "tue" \| "wed" \| "thu" \| "fri" \| "sat"` | 否 | `—` | The day that starts the week. |
| `granularity` | `Granularity` | 否 | `—` | Determines the smallest unit that is displayed in the date picker. By default, this is `"day"` for dates, and `"minute"` for times. |
| `hideTimeZone` | `boolean` | 否 | `false` | Whether to hide the time zone abbreviation. |
| `hourCycle` | `24 \| 12` | 否 | `—` | Whether to display the time in 12 or 24 hour format. By default, this is determined by the user's locale. |
| `isDateUnavailable` | `(date: DateValue, anchorDate: CalendarDate \| null) => boolean` | 否 | `—` | Callback that is called for each date of the calendar. If it returns true, then the date is unavailable. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | 否 | `—` | Whether the input value is invalid. |
| `isOpen` | `boolean` | 否 | `—` | Whether the overlay is open by default (controlled). |
| `isReadOnly` | `boolean` | 否 | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | 否 | `—` | Whether user input is required on the input before form submission. |
| `maxValue` | `DateValue` | 否 | `—` | The maximum allowed date that a user may select. |
| `minValue` | `DateValue` | 否 | `—` | The minimum allowed date that a user may select. |
| `pageBehavior` | `PageBehavior` | 否 | `visible` | Controls the behavior of paging. Pagination either works by advancing the visible page by visibleDuration (default) or one unit of visibleDuration. |
| `placeholderValue` | `T` | 否 | `—` | A placeholder date that influences the format of the placeholder shown when no value is selected. Defaults to today's date at midnight. |
| `render` | `DOMRenderFunction<"div", DateRangePickerRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `shouldCloseOnSelect` | `boolean \| (() => boolean)` | 否 | `true` | Determines whether the date picker popover should close automatically when a date is selected. |
| `shouldForceLeadingZeros` | `boolean` | 否 | `—` | Whether to always show leading zeros in the month, day, and hour fields. By default, this is determined by the user's locale. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `startName` | `string` | 否 | `—` | The name of the start date input element, used when submitting an HTML form. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefname). |
| `style` | `StyleOrFunction<DateRangePickerRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `validate` | `(value: RangeValue<MappedDateValue<T>>) => ValidationError \| true \| null \| undefined` | 否 | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | 否 | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `RangeValue<T>` | 否 | `—` | The current value (controlled). |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: RangeValue<MappedDateValue<T>>) => void` | 否 | `—` | Handler that is called when the value changes. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | 否 | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is released. |
| `onOpenChange` | `(isOpen: boolean) => void` | 否 | `—` | Handler that is called when the overlay's open state changes. |

</details>

## Parts

- `DateRangePicker.Popover`
- `DateRangePicker.RangeSeparator`
- `DateRangePicker.Trigger`
- `DateRangePicker.TriggerIndicator`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17295-58175
