# RangeCalendar

Composable date range picker with month grid, navigation, and year picker support built on React Aria RangeCalendar

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { RangeCalendar } from "@heroui/react";
```

## Figma

[Open RangeCalendar in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17295-56529)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `defaultYearPickerOpen` | `boolean` | No | `—` | — |
| `isYearPickerOpen` | `boolean` | No | `—` | — |
| `onYearPickerOpenChange` | `(isYearPickerOpen: boolean) => void` | No | `—` | — |
| `allowsNonContiguousRanges` | `boolean` | No | `—` | When combined with `isDateUnavailable`, determines whether non-contiguous ranges, i.e. ranges containing unavailable dates, may be selected. |
| `autoFocus` | `boolean` | No | `false` | Whether to automatically focus the calendar when it mounts. |
| `children` | `ChildrenOrFunction<RangeCalendarRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<RangeCalendarRenderProps>` | No | `'react-aria-RangeCalendar'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `commitBehavior` | `"select" \| "clear" \| "reset"` | No | `'select'` | Controls the behavior when a pointer is released outside the calendar or a blur occurs mid selection: - `clear`: clear the currently selected range of dates. - `reset`: reset the selection to the previously selected range of dates. - `select`: select the currently hovered range of dates. |
| `createCalendar` | `(identifier: CalendarIdentifier) => ICalendar` | No | `—` | A function to create a new [Calendar](https://react-spectrum.adobe.com/internationalized/date/Calendar.html) object for a given calendar identifier. If not provided, the `createCalendar` function from `@internationalized/date` will be used. |
| `defaultFocusedValue` | `DateValue` | No | `—` | The date that is focused when the calendar first mounts (uncontrolled). |
| `defaultValue` | `RangeValue<T>` | No | `—` | The default value (uncontrolled). |
| `firstDayOfWeek` | `"sun" \| "mon" \| "tue" \| "wed" \| "thu" \| "fri" \| "sat"` | No | `—` | The day that starts the week. |
| `focusedValue` | `DateValue` | No | `—` | Controls the currently focused date within the calendar. |
| `isDateUnavailable` | `(date: DateValue, anchorDate: CalendarDate \| null) => boolean` | No | `—` | Callback that is called for each date of the calendar. If it returns true, then the date is unavailable. The second argument provides the current selection anchor date, if any. This can be used to adjust the available dates based on the user's first selected date. |
| `isDisabled` | `boolean` | No | `false` | Whether the calendar is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the current selection is invalid according to application logic. |
| `isReadOnly` | `boolean` | No | `false` | Whether the calendar value is immutable. |
| `maxValue` | `DateValue` | No | `—` | The maximum allowed date that a user may select. |
| `minValue` | `DateValue` | No | `—` | The minimum allowed date that a user may select. |
| `onChange` | `(value: RangeValue<MappedDateValue<T>>) => void` | No | `—` | Handler that is called when the value changes. |
| `onFocusChange` | `(date: CalendarDate) => void` | No | `—` | Handler that is called when the focused date changes. |
| `pageBehavior` | `PageBehavior` | No | `visible` | Controls the behavior of paging. Pagination either works by advancing the visible page by visibleDuration (default) or one unit of visibleDuration. |
| `render` | `DOMRenderFunction<"div", RangeCalendarRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectionAlignment` | `"center" \| "end" \| "start"` | No | `'center'` | Determines the alignment of the visible months on initial render based on the current selection or current date if there is no selection. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<RangeCalendarRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `RangeValue<T>` | No | `—` | The current value (controlled). |
| `visibleDuration` | `DateDuration` | No | `{ months: 1 }` | The amount of days that will be displayed at once. This affects how pagination works. |
| `weeksInMonth` | `number` | No | `—` | The number of weeks in a month. This overrides the default set by the locale. |

## Parts

- `RangeCalendar.Cell`
- `RangeCalendar.CellIndicator`
- `RangeCalendar.Grid`
- `RangeCalendar.GridBody`
- `RangeCalendar.GridHeader`
- `RangeCalendar.Header`
- `RangeCalendar.HeaderCell`
- `RangeCalendar.Heading`
- `RangeCalendar.NavButton`
- `RangeCalendar.YearPickerCell`
- `RangeCalendar.YearPickerGrid`
- `RangeCalendar.YearPickerGridBody`
- `RangeCalendar.YearPickerTrigger`
- `RangeCalendar.YearPickerTriggerHeading`
- `RangeCalendar.YearPickerTriggerIndicator`

## Example source

```tsx
'use client';

import {RangeCalendar} from "@heroui/react";

export function Basic() {
  return (
    <RangeCalendar aria-label="Trip dates" firstDayOfWeek="mon">
      <RangeCalendar.Header>
        <RangeCalendar.Heading />
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
    </RangeCalendar>
  );
}

export { Basic as Preview };
```
