# HoloCard

Cube component `HoloCard` from `@bosagent/cube-ui/holo-card`.

Cube component. Source: `packages/cube-ui/src/components/holo-card`.

## Import

```tsx
import { HoloCard } from "@bosagent/cube-ui/holo-card";
import { HoloCard } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `about` | `string` | No | `—` | — |
| `accessKey` | `string` | No | `—` | — |
| `aria-activedescendant` | `string` | No | `—` | — |
| `aria-atomic` | `Booleanish` | No | `—` | — |
| `aria-autocomplete` | `"none" \| "list" \| "both" \| "inline"` | No | `—` | — |
| `aria-braillelabel` | `string` | No | `—` | — |
| `aria-brailleroledescription` | `string` | No | `—` | — |
| `aria-busy` | `Booleanish` | No | `—` | — |
| `aria-checked` | `boolean \| "true" \| "false" \| "mixed"` | No | `—` | — |
| `aria-colcount` | `number` | No | `—` | — |
| `aria-colindex` | `number` | No | `—` | — |
| `aria-colindextext` | `string` | No | `—` | — |
| `aria-colspan` | `number` | No | `—` | — |
| `aria-controls` | `string` | No | `—` | — |
| `aria-current` | `boolean \| "true" \| "false" \| "time" \| "page" \| "date" \| "step" \| "location"` | No | `—` | — |
| `aria-describedby` | `string` | No | `—` | — |
| `aria-description` | `string` | No | `—` | — |
| `aria-details` | `string` | No | `—` | — |
| `aria-disabled` | `Booleanish` | No | `—` | — |
| `aria-dropeffect` | `"link" \| "none" \| "copy" \| "move" \| "execute" \| "popup"` | No | `—` | — |
| `aria-errormessage` | `string` | No | `—` | — |
| `aria-expanded` | `Booleanish` | No | `—` | — |
| `aria-flowto` | `string` | No | `—` | — |
| `aria-grabbed` | `Booleanish` | No | `—` | — |
| `aria-haspopup` | `boolean \| "true" \| "false" \| "dialog" \| "menu" \| "grid" \| "listbox" \| "tree"` | No | `—` | — |
| `aria-hidden` | `Booleanish` | No | `—` | — |
| `aria-invalid` | `boolean \| "true" \| "false" \| "grammar" \| "spelling"` | No | `—` | — |
| `aria-keyshortcuts` | `string` | No | `—` | — |
| `aria-label` | `string` | No | `—` | — |
| `aria-labelledby` | `string` | No | `—` | — |
| `aria-level` | `number` | No | `—` | — |
| `aria-live` | `"off" \| "assertive" \| "polite"` | No | `—` | — |
| `aria-modal` | `Booleanish` | No | `—` | — |
| `aria-multiline` | `Booleanish` | No | `—` | — |
| `aria-multiselectable` | `Booleanish` | No | `—` | — |
| `aria-orientation` | `"horizontal" \| "vertical"` | No | `—` | — |
| `aria-owns` | `string` | No | `—` | — |
| `aria-placeholder` | `string` | No | `—` | — |
| `aria-posinset` | `number` | No | `—` | — |
| `aria-pressed` | `boolean \| "true" \| "false" \| "mixed"` | No | `—` | — |
| `aria-readonly` | `Booleanish` | No | `—` | — |
| `aria-relevant` | `"text" \| "all" \| "additions" \| "additions removals" \| "additions text" \| "removals" \| "removals additions" \| "removals text" \| "text additions" \| "text removals"` | No | `—` | — |
| `aria-required` | `Booleanish` | No | `—` | — |
| `aria-roledescription` | `string` | No | `—` | — |
| `aria-rowcount` | `number` | No | `—` | — |
| `aria-rowindex` | `number` | No | `—` | — |
| `aria-rowindextext` | `string` | No | `—` | — |
| `aria-rowspan` | `number` | No | `—` | — |
| `aria-selected` | `Booleanish` | No | `—` | — |
| `aria-setsize` | `number` | No | `—` | — |
| `aria-sort` | `"none" \| "ascending" \| "descending" \| "other"` | No | `—` | — |
| `aria-valuemax` | `number` | No | `—` | — |
| `aria-valuemin` | `number` | No | `—` | — |
| `aria-valuenow` | `number` | No | `—` | — |
| `aria-valuetext` | `string` | No | `—` | — |
| `autoCapitalize` | `"off" \| "none" \| "on" \| "sentences" \| "words" \| "characters" \| (string & {})` | No | `—` | — |
| `autoCorrect` | `string` | No | `—` | — |
| `autoFocus` | `boolean` | No | `—` | — |
| `autoSave` | `string` | No | `—` | — |

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

## Example source

```tsx
'use client';

import { HoloCard } from '@components/holo-card';

export function Default() {
  return (
    <div className="flex items-center justify-center py-10">
      <HoloCard gradient="linear-gradient(140deg, #3a3730 0%, #1a1b22 78%, #12131c 100%)">
        <HoloCard.Rotator>
          <HoloCard.Frame>
            <HoloCard.Surface>
              <HoloCard.Image
                alt=""
                src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 210 294'%3E%3Cdefs%3E%3ClinearGradient id='g' x1='0' y1='0' x2='1' y2='1'%3E%3Cstop stop-color='%233a3730'/%3E%3Cstop offset='1' stop-color='%2312131c'/%3E%3C/linearGradient%3E%3C/defs%3E%3Crect width='210' height='294' fill='url(%23g)'/%3E%3C/svg%3E"
              />
              <HoloCard.Inset />
              <HoloCard.Pattern />
              <HoloCard.Content className="flex-col items-center justify-center">
                <span className="text-3xl font-bold text-white">
                  Marcus Wong
                </span>
              </HoloCard.Content>
              <HoloCard.Content className="items-end justify-center pb-10">
                <span className="text-sm text-white/40">Member #0999</span>
              </HoloCard.Content>
              <HoloCard.Shine />
            </HoloCard.Surface>
          </HoloCard.Frame>
        </HoloCard.Rotator>
      </HoloCard>
    </div>
  );
}
```
