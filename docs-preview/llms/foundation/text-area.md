# TextArea

Primitive multiline text input component that accepts standard HTML attributes

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：TextArea、text-area。

Native 目录说明：输入多行内容与描述。

## Import

```tsx
import { TextArea } from "@heroui/react";
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
| `variant` | `"primary" \| "secondary"` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `ClassNameOrFunction<InputRenderProps>` | No | `'react-aria-TextArea'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `onHoverChange` | `(isHovering: boolean) => void` | No | `—` | Handler that is called when the hover state changes. |
| `onHoverEnd` | `(e: HoverEvent) => void` | No | `—` | Handler that is called when a hover interaction ends. |
| `onHoverStart` | `(e: HoverEvent) => void` | No | `—` | Handler that is called when a hover interaction starts. |
| `render` | `DOMRenderFunction<"textarea", InputRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | — |
| `style` | `StyleOrFunction<InputRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open TextArea in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-35712)

## 画廊

[TextArea](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/TextArea)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/text-area.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {TextArea} from "@heroui/react";

export function Basic() {
  return (
    <TextArea
      aria-label="Quick project update"
      className="h-32 w-96"
      placeholder="Share a quick project update..."
    />
  );
}

export { Basic as Preview };
```
