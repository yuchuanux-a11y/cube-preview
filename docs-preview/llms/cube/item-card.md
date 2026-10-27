# ItemCard

Cube component `ItemCard` from `@bosagent/cube-ui/item-card`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/item-card` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/item-card` |

检索：ItemCard、item-card。

## Import

```tsx
import { ItemCard } from "@bosagent/cube-ui/item-card";
import { ItemCard } from "@bosagent/cube-ui";
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
| `variant` | `"outline" \| "default" \| "secondary" \| "tertiary" \| "transparent"` | No | `"default"` | Visual variant. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Parts

- `ItemCard.Action`
- `ItemCard.Content`
- `ItemCard.Description`
- `ItemCard.Icon`
- `ItemCard.Title`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ItemCard](https://yuchuanux-a11y.github.io/cube-preview/#ItemCard)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/item-card.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { ItemCard } from '@components/item-card';
import { CircleChevronRight, Globe } from '@gravity-ui/icons';
import { Button } from '@heroui/react';

export function Default() {
  return (
    <div className="w-[500px] rounded-2xl p-6">
      <ItemCard>
        <ItemCard.Icon>
          <Globe />
        </ItemCard.Icon>
        <ItemCard.Content>
          <ItemCard.Title>Language</ItemCard.Title>
          <ItemCard.Description>
            Choose your preferred language
          </ItemCard.Description>
        </ItemCard.Content>
        <ItemCard.Action>
          <Button size="sm" variant="outline">
            English
            <CircleChevronRight className="size-3.5" />
          </Button>
        </ItemCard.Action>
      </ItemCard>
    </div>
  );
}
```
