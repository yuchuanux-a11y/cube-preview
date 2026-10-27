# TextShimmer

Cube component `TextShimmer` from `@bosagent/cube-ui/text-shimmer`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/text-shimmer` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/text-shimmer` |

检索：TextShimmer、text-shimmer。

## Import

```tsx
import { TextShimmer } from "@bosagent/cube-ui/text-shimmer";
import { TextShimmer } from "@bosagent/cube-ui";
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
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[TextShimmer](https://yuchuanux-a11y.github.io/cube-preview/#TextShimmer)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/text-shimmer.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { TextShimmer } from '@components/text-shimmer';

export function Default() {
  return (
    <div className="flex flex-col gap-4 text-sm">
      <TextShimmer>Thinking...</TextShimmer>
      <TextShimmer>Generating response...</TextShimmer>
    </div>
  );
}
```
