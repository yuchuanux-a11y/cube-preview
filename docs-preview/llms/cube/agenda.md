# Agenda

Cube component `Agenda` from `@bosagent/cube-ui/agenda`.

- 分层：Cube
- 包：`@bosagent/cube-ui/agenda`
- 状态：建设中

## Import

```tsx
import { Agenda } from "@bosagent/cube-ui/agenda";
import { Agenda } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `allDayCountPerDay` | `number[]` | 是 | `—` | — |
| `allDayEvents` | `AgendaEventData[]` | 是 | `—` | — |
| `allDayLayout` | `AllDayLayoutItem[]` | 是 | `—` | — |
| `children` | `ReactNode` | 是 | `—` | — |
| `date` | `CalendarDate` | 是 | `—` | — |
| `dragState` | `DragState` | 是 | `—` | — |
| `dropPreview` | `DropPreview` | 是 | `—` | — |
| `endHour` | `number` | 是 | `—` | — |
| `events` | `AgendaEventData[]` | 是 | `—` | — |
| `getAllEventsForDay` | `(date: CalendarDate) => AgendaEventData[]` | 是 | `—` | — |
| `getEventLayout` | `(eventId: string) => { columnIndex: number; totalColumns: number; }` | 是 | `—` | — |
| `getEventsForDay` | `(date: CalendarDate) => AgendaEventData[]` | 是 | `—` | — |
| `getMonthRowLayout` | `(week: CalendarDate[]) => MonthRowLayout` | 是 | `—` | — |
| `getPerCellEvents` | `(day: CalendarDate, week: CalendarDate[]) => AgendaEventData[]` | 是 | `—` | — |
| `goToNext` | `() => void` | 是 | `—` | — |
| `goToPrevious` | `() => void` | 是 | `—` | — |
| `goToToday` | `() => void` | 是 | `—` | — |
| `heading` | `string` | 是 | `—` | — |
| `isAllDayExpanded` | `boolean` | 是 | `—` | — |
| `locale` | `string` | 是 | `—` | — |
| `selectedEventId` | `string` | 是 | `—` | — |
| `selectEvent` | `(id: string \| null) => void` | 是 | `—` | — |
| `setDate` | `(date: CalendarDate) => void` | 是 | `—` | — |
| `setDragState` | `React.Dispatch<React.SetStateAction<DragState>>` | 是 | `—` | — |
| `setDropPreview` | `React.Dispatch<React.SetStateAction<DropPreview>>` | 是 | `—` | — |
| `setView` | `(view: AgendaView) => void` | 是 | `—` | — |
| `slotDuration` | `number` | 是 | `—` | — |
| `slots` | `{ allDaySection: (slotProps?: { view?: "week" \| "day" \| "month"; } & ClassProp<ClassNameValue>) => string; base: (slotProps?: { view?: "week" \| "day" \| "month"; } & ClassProp<Clas…` | 是 | `—` | — |
| `startHour` | `number` | 是 | `—` | — |
| `timeZone` | `string` | 是 | `—` | — |
| `toggleAllDayExpanded` | `() => void` | 是 | `—` | — |
| `view` | `AgendaView` | 是 | `—` | — |
| `visibleDays` | `CalendarDate[]` | 是 | `—` | — |
| `visibleWeeks` | `CalendarDate[][]` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onEventCreate` | `(event: { start: CalendarDateTime; end: CalendarDateTime; }) => void` | 否 | `—` | — |
| `onEventDelete` | `(id: string) => void` | 否 | `—` | — |
| `onEventMove` | `(id: string, start: CalendarDateTime, end: CalendarDateTime) => void` | 否 | `—` | — |
| `onEventResize` | `(id: string, start: CalendarDateTime, end: CalendarDateTime) => void` | 否 | `—` | — |

</details>

## Parts

- `Agenda.AllDayEvent`
- `Agenda.AllDayLabel`
- `Agenda.AllDaySection`
- `Agenda.Body`
- `Agenda.CurrentTimeIndicator`
- `Agenda.DayColumn`
- `Agenda.DayHeader`
- `Agenda.Event`
- `Agenda.EventTime`
- `Agenda.EventTitle`
- `Agenda.Header`
- `Agenda.Heading`
- `Agenda.MonthCell`
- `Agenda.MonthEvent`
- `Agenda.MonthGrid`
- `Agenda.MonthRow`
- `Agenda.MonthSpanningEvent`
- `Agenda.NavButton`
- `Agenda.Navigation`
- `Agenda.TimeGrid`
- `Agenda.TodayButton`
- `Agenda.ViewSelector`
- `Agenda.WeekHeader`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Agenda
