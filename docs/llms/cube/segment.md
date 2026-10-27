# Segment

Cube component `Segment` from `@bosagent/cube-ui/segment`.

Cube component. Source: `packages/cube-ui/src/components/segment`.

## Import

```tsx
import { Segment } from "@bosagent/cube-ui/segment";
import { Segment } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `className` | `string` | No | `'react-aria-ToggleButtonGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultSelectedKey` | `Key` | No | `—` | — |
| `isDisabled` | `boolean` | No | `—` | Whether all items are disabled. |
| `onSelectionChange` | `(key: Key) => void` | No | `—` | — |
| `selectedKey` | `Key` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `variant` | `"default" \| "ghost"` | No | `—` | — |
| `children` | `ChildrenOrFunction<ToggleButtonGroupRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `disallowEmptySelection` | `boolean` | No | `—` | Whether the collection allows empty selection. |
| `orientation` | `Orientation` | No | `'horizontal'` | The orientation of the the toggle button group. |
| `render` | `DOMRenderFunction<"div", ToggleButtonGroupRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ToggleButtonGroupRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `Segment.Item`
- `Segment.Separator`

## Example source

```tsx
'use client';

import { Segment } from '@components/segment';

const tabs = [
  { id: 'dashboard', label: 'Dashboard' },
  { id: 'analytics', label: 'Analytics' },
  { id: 'reports', label: 'Reports' },
  { id: 'settings', label: 'Settings' },
];

export function Default() {
  return (
    <Segment defaultSelectedKey="dashboard">
      {tabs.map((tab) => (
        <Segment.Item key={tab.id} id={tab.id}>
          <Segment.Separator />
          {tab.label}
        </Segment.Item>
      ))}
    </Segment>
  );
}
```
