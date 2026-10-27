# Calendar

Composable date picker with month grid, navigation, and year picker support built on React Aria Calendar

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：Calendar、calendar。

## Import

```tsx
import { Calendar } from "@heroui/react";
```

## Preview

The docs page renders a live preview of the real component.

## 适用

建设中。设计 registry 没有这条用法。

## 不适用

建设中。

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `defaultYearPickerOpen` | `boolean` | No | `—` | — |
| `isYearPickerOpen` | `boolean` | No | `—` | — |
| `onYearPickerOpenChange` | `(isYearPickerOpen: boolean) => void` | No | `—` | — |
| `autoFocus` | `boolean` | No | `false` | Whether to automatically focus the calendar when it mounts. |
| `children` | `ChildrenOrFunction<CalendarRenderProps<M>>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<CalendarRenderProps<M>>` | No | `'react-aria-Calendar'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `createCalendar` | `(identifier: CalendarIdentifier) => ICalendar` | No | `—` | A function to create a new [Calendar](https://react-spectrum.adobe.com/internationalized/date/Calendar.html) object for a given calendar identifier. If not provided, the `createCalendar` function from `@internationalized/date` will be used. |
| `defaultFocusedValue` | `DateValue` | No | `—` | The date that is focused when the calendar first mounts (uncontrolled). |
| `defaultValue` | `CalendarValueType<T, M>` | No | `—` | The default value (uncontrolled). |
| `firstDayOfWeek` | `"sun" \| "mon" \| "tue" \| "wed" \| "thu" \| "fri" \| "sat"` | No | `—` | The day that starts the week. |
| `focusedValue` | `DateValue` | No | `—` | Controls the currently focused date within the calendar. |
| `isDateUnavailable` | `(date: DateValue) => boolean` | No | `—` | Callback that is called for each date of the calendar. If it returns true, then the date is unavailable. |
| `isDisabled` | `boolean` | No | `false` | Whether the calendar is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the current selection is invalid according to application logic. |
| `isReadOnly` | `boolean` | No | `false` | Whether the calendar value is immutable. |
| `maxValue` | `DateValue` | No | `—` | The maximum allowed date that a user may select. |
| `minValue` | `DateValue` | No | `—` | The minimum allowed date that a user may select. |
| `onChange` | `(value: CalendarValueType<MappedDateValue<T>, M>) => void` | No | `—` | Handler that is called when the value changes. |
| `onFocusChange` | `(date: CalendarDate) => void` | No | `—` | Handler that is called when the focused date changes. |
| `pageBehavior` | `PageBehavior` | No | `visible` | Controls the behavior of paging. Pagination either works by advancing the visible page by visibleDuration (default) or one unit of visibleDuration. |
| `render` | `DOMRenderFunction<"div", CalendarRenderProps<M>>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectionAlignment` | `"center" \| "end" \| "start"` | No | `'center'` | Determines the alignment of the visible months on initial render based on the current selection or current date if there is no selection. |
| `selectionMode` | `M` | No | `'single'` | Whether single or multiple selection is enabled. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<CalendarRenderProps<M>>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `CalendarValueType<T, M>` | No | `—` | The current value (controlled). |
| `visibleDuration` | `DateDuration` | No | `{ months: 1 }` | The amount of days that will be displayed at once. This affects how pagination works. |
| `weeksInMonth` | `number` | No | `—` | The number of weeks in a month. This overrides the default set by the locale. |

## Parts

- `Calendar.Cell`
- `Calendar.CellIndicator`
- `Calendar.Grid`
- `Calendar.GridBody`
- `Calendar.GridHeader`
- `Calendar.Header`
- `Calendar.HeaderCell`
- `Calendar.Heading`
- `Calendar.NavButton`
- `Calendar.YearPickerCell`
- `Calendar.YearPickerGrid`
- `Calendar.YearPickerGridBody`
- `Calendar.YearPickerTrigger`
- `Calendar.YearPickerTriggerHeading`
- `Calendar.YearPickerTriggerIndicator`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open Calendar in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-71626)

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/calendar.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Calendar} from "@heroui/react";

export function Basic() {
  return (
    <Calendar aria-label="Event date">
      <Calendar.Header>
        <Calendar.Heading />
        <Calendar.NavButton slot="previous" />
        <Calendar.NavButton slot="next" />
      </Calendar.Header>
      <Calendar.Grid>
        <Calendar.GridHeader>
          {(day) => <Calendar.HeaderCell>{day}</Calendar.HeaderCell>}
        </Calendar.GridHeader>
        <Calendar.GridBody>{(date) => <Calendar.Cell date={date} />}</Calendar.GridBody>
      </Calendar.Grid>
    </Calendar>
  );
}

export { Basic as Preview };
```
