# Skeleton

Skeleton is a placeholder to show a loading state and the expected shape of a component.

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：Skeleton、skeleton。

Native 目录说明：为加载中的内容预留结构。

## Import

```tsx
import { Skeleton } from "@heroui/react";
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
| `animationType` | `"none" \| "pulse" \| "shimmer"` | No | `—` | Animation type. |
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `children` | `JSX.IntrinsicElements[E]["children"]` | No | `—` | — |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open Skeleton in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=6141-14118)

## 画廊

[Skeleton](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Skeleton)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/skeleton.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Skeleton} from "@heroui/react";

export function Basic() {
  return (
    <div className="shadow-panel w-[250px] space-y-5 rounded-lg bg-transparent p-4">
      <Skeleton className="h-32 rounded-lg" />
      <div className="space-y-3">
        <Skeleton className="h-3 w-3/5 rounded-lg" />
        <Skeleton className="h-3 w-4/5 rounded-lg" />
        <Skeleton className="h-3 w-2/5 rounded-lg" />
      </div>
    </div>
  );
}

export { Basic as Preview };
```
