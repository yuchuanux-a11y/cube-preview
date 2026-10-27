# Tabs

Tabs organize content into multiple sections and allow users to navigate between them.

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：Tabs、tabs。

Native 目录说明：在相关内容视图间切换。

## Import

```tsx
import { Tabs } from "@heroui/react";
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
| `children` | `ReactNode` | Yes | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `align` | `"center" \| "end" \| "start"` | No | `—` | — |
| `className` | `string` | No | `'react-aria-Tabs'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `variant` | `"primary" \| "secondary"` | No | `—` | — |
| `defaultSelectedKey` | `Key` | No | `—` | The initial selected keys in the collection (uncontrolled). |
| `disabledKeys` | `Iterable<Key>` | No | `—` | The item keys that are disabled. These items cannot be selected, focused, or otherwise interacted with. |
| `isDisabled` | `boolean` | No | `—` | Whether the TabList is disabled. Shows that a selection exists, but is not available in that circumstance. |
| `keyboardActivation` | `"manual" \| "automatic"` | No | `'automatic'` | Whether tabs are activated automatically on focus or manually. |
| `onSelectionChange` | `(key: Key) => void` | No | `—` | Handler that is called when the selection changes. |
| `orientation` | `Orientation` | No | `'horizontal'` | The orientation of the tabs. |
| `render` | `DOMRenderFunction<"div", TabsRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `selectedKey` | `Key` | No | `—` | The currently selected key in the collection (controlled). |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<TabsRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `Tabs.Indicator`
- `Tabs.List`
- `Tabs.ListContainer`
- `Tabs.Panel`
- `Tabs.Separator`
- `Tabs.Tab`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open Tabs in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-79785)

## 画廊

[Tabs](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Tabs)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/tabs.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Tabs} from "@heroui/react";

const listClassName = [
  "rounded-xl border border-accent/10 bg-accent-soft/30 p-1",
  "**:data-[slot=tabs-tab]:rounded-lg",
  "**:data-[slot=tabs-tab]:bg-transparent",
  "**:data-[slot=tabs-tab]:text-muted",
  "**:data-[slot=tabs-tab]:opacity-100",
  "**:data-[slot=tabs-tab]:transition-colors",
  "**:data-[slot=tabs-tab]:data-[hovered=true]:not-data-[selected=true]:bg-accent-soft",
  "**:data-[slot=tabs-tab]:data-[hovered=true]:not-data-[selected=true]:text-accent-soft-foreground",
  "**:data-[slot=tabs-tab]:data-[pressed=true]:not-data-[selected=true]:bg-accent-soft-hover",
  "**:data-[slot=tabs-tab]:data-[focus-visible=true]:ring-2",
  "**:data-[slot=tabs-tab]:data-[focus-visible=true]:ring-accent/15",
  "**:data-[slot=tabs-tab]:data-[selected=true]:font-medium",
  "**:data-[slot=tabs-tab]:data-[selected=true]:text-accent-foreground",
  "**:data-[slot=tabs-tab]:shadow-none",
  "**:data-[slot=tabs-indicator]:rounded-lg",
  "**:data-[slot=tabs-indicator]:bg-accent",
  "**:data-[slot=tabs-indicator]:shadow-none",
].join(" ");

export function CustomStyles() {
  return (
    <Tabs className="w-full max-w-sm">
      <Tabs.ListContainer className="rounded-none bg-transparent">
        <Tabs.List aria-label="Billing cycle" className={listClassName}>
          <Tabs.Tab id="monthly">
            Monthly
            <Tabs.Indicator />
          </Tabs.Tab>
          <Tabs.Tab id="yearly">
            Yearly
            <Tabs.Indicator />
          </Tabs.Tab>
        </Tabs.List>
      </Tabs.ListContainer>
      <Tabs.Panel className="pt-3 text-sm text-muted" id="monthly">
        Billed monthly, cancel anytime.
      </Tabs.Panel>
      <Tabs.Panel className="pt-3 text-sm text-muted" id="yearly">
        Save 20% with annual billing.
      </Tabs.Panel>
    </Tabs>
  );
}

export { CustomStyles as Preview };
```
