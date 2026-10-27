# ToggleButtonGroup

Groups multiple ToggleButtons into a unified control, allowing users to select one or multiple options.

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：ToggleButtonGroup、toggle-button-group。

## Import

```tsx
import { ToggleButtonGroup } from "@heroui/react";
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
| `fullWidth` | `boolean` | No | `—` | — |
| `isDetached` | `boolean` | No | `—` | Whether the group buttons are visually separated (detached) instead of connected |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | Size to propagate to all child ToggleButtons |
| `children` | `ChildrenOrFunction<ToggleButtonGroupRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ToggleButtonGroupRenderProps>` | No | `'react-aria-ToggleButtonGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultSelectedKeys` | `Iterable<Key>` | No | `—` | The initial selected keys in the collection (uncontrolled). |
| `disallowEmptySelection` | `boolean` | No | `—` | Whether the collection allows empty selection. |
| `isDisabled` | `boolean` | No | `—` | Whether all items are disabled. |
| `onSelectionChange` | `(keys: Set<Key>) => void` | No | `—` | Handler that is called when the selection changes. |
| `orientation` | `Orientation` | No | `'horizontal'` | The orientation of the the toggle button group. |
| `render` | `DOMRenderFunction<"div", ToggleButtonGroupRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKeys` | `Iterable<Key>` | No | `—` | The currently selected keys in the collection (controlled). |
| `selectionMode` | `"single" \| "multiple"` | No | `'single'` | Whether single or multiple selection is enabled. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ToggleButtonGroupRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `ToggleButtonGroup.Separator`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open ToggleButtonGroup in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=15251-25651)

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/toggle-button-group.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Bold, Italic, Strikethrough, Underline} from "@gravity-ui/icons";
import {ToggleButton, ToggleButtonGroup} from "@heroui/react";

export function Basic() {
  return (
    <ToggleButtonGroup selectionMode="multiple">
      <ToggleButton isIconOnly aria-label="Bold" id="bold">
        <Bold />
      </ToggleButton>
      <ToggleButton isIconOnly aria-label="Italic" id="italic">
        <ToggleButtonGroup.Separator />
        <Italic />
      </ToggleButton>
      <ToggleButton isIconOnly aria-label="Underline" id="underline">
        <ToggleButtonGroup.Separator />
        <Underline />
      </ToggleButton>
      <ToggleButton isIconOnly aria-label="Strikethrough" id="strikethrough">
        <ToggleButtonGroup.Separator />
        <Strikethrough />
      </ToggleButton>
    </ToggleButtonGroup>
  );
}

export { Basic as Preview };
```
