# CellSlider

Cube component `CellSlider` from `@bosagent/cube-ui/cell-slider`.

Cube component. Source: `packages/cube-ui/src/components/cell-slider`.

## Import

```tsx
import { CellSlider } from "@bosagent/cube-ui/cell-slider";
import { CellSlider } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `variant` | `"default" \| "secondary"` | No | `"default"` | Visual variant. |
| `children` | `ChildrenOrFunction<SliderRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<SliderRenderProps>` | No | `'react-aria-Slider'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `number \| number[]` | No | `—` | The default value (uncontrolled). |
| `formatOptions` | `Intl.NumberFormatOptions` | No | `—` | The display format of the value label. |
| `isDisabled` | `boolean` | No | `—` | Whether the whole Slider is disabled. |
| `maxValue` | `number` | No | `100` | The slider's maximum value. |
| `minValue` | `number` | No | `0` | The slider's minimum value. |
| `onChange` | `(value: number \| number[]) => void` | No | `—` | Handler that is called when the value changes. |
| `onChangeEnd` | `(value: number \| number[]) => void` | No | `—` | Fired when the slider stops moving, due to being let go. |
| `render` | `DOMRenderFunction<"div", SliderRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `step` | `number` | No | `1` | The slider's step value. |
| `style` | `StyleOrFunction<SliderRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `value` | `number \| number[]` | No | `—` | The current value (controlled). |

## Parts

- `CellSlider.Fill`
- `CellSlider.Label`
- `CellSlider.Output`
- `CellSlider.Thumb`
- `CellSlider.Track`

## Example source

```tsx
'use client';

import { CellSlider } from '@components/cell-slider';

export function Default() {
  return (
    <div className="w-[252px]">
      <CellSlider
        aria-label="Spacing"
        defaultValue={0.5}
        formatOptions={{ maximumFractionDigits: 2, minimumFractionDigits: 2 }}
        maxValue={1}
        minValue={0}
        step={0.01}
      >
        <CellSlider.Track>
          <CellSlider.Fill />
          <CellSlider.Thumb />
          <CellSlider.Label>Spacing</CellSlider.Label>
          <CellSlider.Output />
        </CellSlider.Track>
      </CellSlider>
    </div>
  );
}
```
