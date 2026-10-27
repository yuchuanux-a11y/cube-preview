# ProgressBar

A progress bar shows either determinate or indeterminate progress of an operation over time.

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { ProgressBar } from "@heroui/react";
```

## Figma

[Open ProgressBar in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=21302-78002)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `color` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `children` | `ChildrenOrFunction<ProgressBarRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ProgressBarRenderProps>` | No | `'react-aria-ProgressBar'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `formatOptions` | `Intl.NumberFormatOptions` | No | `{ style: 'percent' }` | The display format of the value label. |
| `isIndeterminate` | `boolean` | No | `—` | Whether presentation is indeterminate when progress isn't known. |
| `maxValue` | `number` | No | `100` | The largest value allowed for the input. |
| `minValue` | `number` | No | `0` | The smallest value allowed for the input. |
| `render` | `DOMRenderFunction<"div", ProgressBarRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ProgressBarRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `number` | No | `0` | The current value (controlled). |
| `valueLabel` | `ReactNode` | No | `—` | The content to display as the value's label (e.g. 1 of 4). |

## Parts

- `ProgressBar.Fill`
- `ProgressBar.Output`
- `ProgressBar.Track`

## Example source

```tsx
'use client';

import {Label, ProgressBar} from "@heroui/react";

export function Basic() {
  return (
    <ProgressBar aria-label="Loading" className="w-64" value={60}>
      <Label>Loading</Label>
      <ProgressBar.Output />
      <ProgressBar.Track>
        <ProgressBar.Fill />
      </ProgressBar.Track>
    </ProgressBar>
  );
}

export { Basic as Preview };
```
