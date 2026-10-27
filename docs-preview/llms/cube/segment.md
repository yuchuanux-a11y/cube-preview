# Segment

Cube component `Segment` from `@bosagent/cube-ui/segment`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/segment` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/segment` |

检索：Segment、segment。

## Import

```tsx
import { Segment } from "@bosagent/cube-ui/segment";
import { Segment } from "@bosagent/cube-ui";
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

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[Segment](https://yuchuanux-a11y.github.io/cube-preview/#Segment)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/segment.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

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
