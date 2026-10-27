# Tooltip

Displays informative text when users hover over or focus on an element

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Tooltip } from "@heroui/react";
```

## Figma

[Open Tooltip in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-71565)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `shouldSkipAnimation` | `boolean` | No | `false` | Whether to let React Aria skip the enter and exit animations while its global warmup timer is active, i.e. when moving quickly from one tooltip to another. |
| `children` | `React.ReactNode` | Yes | `—` | — |
| `closeDelay` | `number` | No | `500` | The delay time for the tooltip to close. [See guidelines](https://spectrum.adobe.com/page/tooltip/#Warmup-and-cooldown). |
| `defaultOpen` | `boolean` | No | `—` | Whether the overlay is open by default (uncontrolled). |
| `delay` | `number` | No | `1500` | The delay time for the tooltip to show up. [See guidelines](https://spectrum.adobe.com/page/tooltip/#Immediate-or-delayed-appearance). |
| `isDisabled` | `boolean` | No | `—` | Whether the tooltip should be disabled, independent from the trigger. |
| `isOpen` | `boolean` | No | `—` | Whether the overlay is open by default (controlled). |
| `onOpenChange` | `(isOpen: boolean) => void` | No | `—` | Handler that is called when the overlay's open state changes. |
| `shouldCloseOnPress` | `boolean` | No | `true` | Whether the tooltip should close when the trigger is pressed. |
| `trigger` | `"focus" \| "hover"` | No | `'hover'` | By default, opens for both focus and hover. Can be made to open only for focus. |

## Parts

- `Tooltip.Arrow`
- `Tooltip.Content`
- `Tooltip.Trigger`

## Example source

```tsx
'use client';

import {CircleInfo} from "@gravity-ui/icons";
import {Button, Tooltip} from "@heroui/react";

export function TooltipBasic() {
  return (
    <div className="flex items-center gap-4">
      <Tooltip delay={0}>
        <Button variant="secondary">Hover me</Button>
        <Tooltip.Content>
          <p>This is a tooltip</p>
        </Tooltip.Content>
      </Tooltip>

      <Tooltip delay={0}>
        <Button isIconOnly aria-label="More information" variant="tertiary">
          <CircleInfo />
        </Button>
        <Tooltip.Content>
          <p>More information</p>
        </Tooltip.Content>
      </Tooltip>
    </div>
  );
}

export { TooltipBasic as Preview };
```
