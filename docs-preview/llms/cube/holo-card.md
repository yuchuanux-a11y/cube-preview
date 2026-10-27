# HoloCard

Cube component `HoloCard` from `@bosagent/cube-ui/holo-card`.

- 分层：Cube
- 包：`@bosagent/cube-ui/holo-card`
- 状态：建设中

## Import

```tsx
import { HoloCard } from "@bosagent/cube-ui/holo-card";
import { HoloCard } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `about` | `string` | 否 | `—` | — |
| `accessKey` | `string` | 否 | `—` | — |
| `autoCapitalize` | `"off" \| "none" \| "on" \| "sentences" \| "words" \| "characters" \| (string & {})` | 否 | `—` | — |
| `autoCorrect` | `string` | 否 | `—` | — |
| `autoFocus` | `boolean` | 否 | `—` | — |
| `autoSave` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `aria-activedescendant` | `string` | 否 | `—` | — |
| `aria-atomic` | `Booleanish` | 否 | `—` | — |
| `aria-autocomplete` | `"none" \| "list" \| "both" \| "inline"` | 否 | `—` | — |
| `aria-braillelabel` | `string` | 否 | `—` | — |
| `aria-brailleroledescription` | `string` | 否 | `—` | — |
| `aria-busy` | `Booleanish` | 否 | `—` | — |
| `aria-checked` | `boolean \| "true" \| "false" \| "mixed"` | 否 | `—` | — |
| `aria-colcount` | `number` | 否 | `—` | — |
| `aria-colindex` | `number` | 否 | `—` | — |
| `aria-colindextext` | `string` | 否 | `—` | — |
| `aria-colspan` | `number` | 否 | `—` | — |
| `aria-controls` | `string` | 否 | `—` | — |
| `aria-current` | `boolean \| "true" \| "false" \| "time" \| "page" \| "date" \| "step" \| "location"` | 否 | `—` | — |
| `aria-describedby` | `string` | 否 | `—` | — |
| `aria-description` | `string` | 否 | `—` | — |
| `aria-details` | `string` | 否 | `—` | — |
| `aria-disabled` | `Booleanish` | 否 | `—` | — |
| `aria-dropeffect` | `"link" \| "none" \| "copy" \| "move" \| "execute" \| "popup"` | 否 | `—` | — |
| `aria-errormessage` | `string` | 否 | `—` | — |
| `aria-expanded` | `Booleanish` | 否 | `—` | — |
| `aria-flowto` | `string` | 否 | `—` | — |
| `aria-grabbed` | `Booleanish` | 否 | `—` | — |
| `aria-haspopup` | `boolean \| "true" \| "false" \| "dialog" \| "menu" \| "grid" \| "listbox" \| "tree"` | 否 | `—` | — |
| `aria-hidden` | `Booleanish` | 否 | `—` | — |
| `aria-invalid` | `boolean \| "true" \| "false" \| "grammar" \| "spelling"` | 否 | `—` | — |
| `aria-keyshortcuts` | `string` | 否 | `—` | — |
| `aria-label` | `string` | 否 | `—` | — |
| `aria-labelledby` | `string` | 否 | `—` | — |
| `aria-level` | `number` | 否 | `—` | — |
| `aria-live` | `"off" \| "assertive" \| "polite"` | 否 | `—` | — |
| `aria-modal` | `Booleanish` | 否 | `—` | — |
| `aria-multiline` | `Booleanish` | 否 | `—` | — |
| `aria-multiselectable` | `Booleanish` | 否 | `—` | — |
| `aria-orientation` | `"horizontal" \| "vertical"` | 否 | `—` | — |
| `aria-owns` | `string` | 否 | `—` | — |
| `aria-placeholder` | `string` | 否 | `—` | — |
| `aria-posinset` | `number` | 否 | `—` | — |
| `aria-pressed` | `boolean \| "true" \| "false" \| "mixed"` | 否 | `—` | — |
| `aria-readonly` | `Booleanish` | 否 | `—` | — |
| `aria-relevant` | `"text" \| "all" \| "additions" \| "additions removals" \| "additions text" \| "removals" \| "removals additions" \| "removals text" \| "text additions" \| "text removals"` | 否 | `—` | — |
| `aria-required` | `Booleanish` | 否 | `—` | — |
| `aria-roledescription` | `string` | 否 | `—` | — |
| `aria-rowcount` | `number` | 否 | `—` | — |
| `aria-rowindex` | `number` | 否 | `—` | — |
| `aria-rowindextext` | `string` | 否 | `—` | — |
| `aria-rowspan` | `number` | 否 | `—` | — |
| `aria-selected` | `Booleanish` | 否 | `—` | — |
| `aria-setsize` | `number` | 否 | `—` | — |
| `aria-sort` | `"none" \| "ascending" \| "descending" \| "other"` | 否 | `—` | — |
| `aria-valuemax` | `number` | 否 | `—` | — |
| `aria-valuemin` | `number` | 否 | `—` | — |
| `aria-valuenow` | `number` | 否 | `—` | — |
| `aria-valuetext` | `string` | 否 | `—` | — |

</details>

## Parts

- `HoloCard.Content`
- `HoloCard.Frame`
- `HoloCard.Image`
- `HoloCard.Inset`
- `HoloCard.Pattern`
- `HoloCard.Rotator`
- `HoloCard.Shine`
- `HoloCard.ShinePattern`
- `HoloCard.Surface`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#HoloCard
