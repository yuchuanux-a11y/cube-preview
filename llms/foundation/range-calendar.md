# RangeCalendar

Composable date range picker with month grid, navigation, and year picker support built on React Aria RangeCalendar

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { RangeCalendar } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `defaultYearPickerOpen` | `boolean` | 否 | `—` | — |
| `isYearPickerOpen` | `boolean` | 否 | `—` | — |
| `allowsNonContiguousRanges` | `boolean` | 否 | `—` | When combined with `isDateUnavailable`, determines whether non-contiguous ranges, i.e. ranges containing unavailable dates, may be selected. |
| `autoFocus` | `boolean` | 否 | `false` | Whether to automatically focus the calendar when it mounts. |
| `children` | `ChildrenOrFunction<RangeCalendarRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<RangeCalendarRenderProps>` | 否 | `'react-aria-RangeCalendar'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `commitBehavior` | `"select" \| "clear" \| "reset"` | 否 | `'select'` | Controls the behavior when a pointer is released outside the calendar or a blur occurs mid selection: - `clear`: clear the currently selected range of dates. - `reset`: reset the selection to the previously selected range of dates. - `select`: select the currently hovered range of dates. |
| `createCalendar` | `(identifier: CalendarIdentifier) => ICalendar` | 否 | `—` | A function to create a new [Calendar](https://react-spectrum.adobe.com/internationalized/date/Calendar.html) object for a given calendar identifier. If not provided, the `createCalendar` function from `@internationalized/date` will be used. |
| `defaultFocusedValue` | `DateValue` | 否 | `—` | The date that is focused when the calendar first mounts (uncontrolled). |
| `defaultValue` | `RangeValue<T>` | 否 | `—` | The default value (uncontrolled). |
| `firstDayOfWeek` | `"sun" \| "mon" \| "tue" \| "wed" \| "thu" \| "fri" \| "sat"` | 否 | `—` | The day that starts the week. |
| `focusedValue` | `DateValue` | 否 | `—` | Controls the currently focused date within the calendar. |
| `isDateUnavailable` | `(date: DateValue, anchorDate: CalendarDate \| null) => boolean` | 否 | `—` | Callback that is called for each date of the calendar. If it returns true, then the date is unavailable. The second argument provides the current selection anchor date, if any. This can be used to adjust the available dates based on the user's first selected date. |
| `isDisabled` | `boolean` | 否 | `false` | Whether the calendar is disabled. |
| `isInvalid` | `boolean` | 否 | `—` | Whether the current selection is invalid according to application logic. |
| `isReadOnly` | `boolean` | 否 | `false` | Whether the calendar value is immutable. |
| `maxValue` | `DateValue` | 否 | `—` | The maximum allowed date that a user may select. |
| `minValue` | `DateValue` | 否 | `—` | The minimum allowed date that a user may select. |
| `pageBehavior` | `PageBehavior` | 否 | `visible` | Controls the behavior of paging. Pagination either works by advancing the visible page by visibleDuration (default) or one unit of visibleDuration. |
| `render` | `DOMRenderFunction<"div", RangeCalendarRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectionAlignment` | `"center" \| "end" \| "start"` | 否 | `'center'` | Determines the alignment of the visible months on initial render based on the current selection or current date if there is no selection. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<RangeCalendarRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `RangeValue<T>` | 否 | `—` | The current value (controlled). |
| `visibleDuration` | `DateDuration` | 否 | `{ months: 1 }` | The amount of days that will be displayed at once. This affects how pagination works. |
| `weeksInMonth` | `number` | 否 | `—` | The number of weeks in a month. This overrides the default set by the locale. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onYearPickerOpenChange` | `(isYearPickerOpen: boolean) => void` | 否 | `—` | — |
| `onChange` | `(value: RangeValue<MappedDateValue<T>>) => void` | 否 | `—` | Handler that is called when the value changes. |
| `onFocusChange` | `(date: CalendarDate) => void` | 否 | `—` | Handler that is called when the focused date changes. |

</details>

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

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17295-56529
