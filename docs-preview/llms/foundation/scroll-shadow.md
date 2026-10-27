# ScrollShadow

Apply visual shadows to indicate scrollable content overflow with automatic detection of scroll position.

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：ScrollShadow、scroll-shadow。

Native 目录说明：提示可滚动区域与内容边界。

## Import

```tsx
import { ScrollShadow } from "@heroui/react";
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
| `hideScrollBar` | `boolean` | No | `—` | — |
| `isEnabled` | `boolean` | No | `true` | Whether scroll shadow detection is enabled |
| `offset` | `number` | No | `0` | The scroll offset before showing shadows (in pixels) |
| `onVisibilityChange` | `(visibility: ScrollShadowVisibility) => void` | No | `—` | Callback invoked when shadow visibility changes |
| `orientation` | `"horizontal" \| "vertical"` | No | `—` | — |
| `size` | `number` | No | `40` | The shadow size in pixels |
| `variant` | `"fade"` | No | `—` | — |
| `visibility` | `ScrollShadowVisibility` | No | `"auto"` | Controlled shadow visibility state |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open ScrollShadow in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-73776)

## 画廊

[ScrollShadow](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/ScrollShadow)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/scroll-shadow.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import type {ScrollShadowVisibility} from "@heroui/react";

import {Card, ScrollShadow} from "@heroui/react";
import {useState} from "react";

const images = [
  "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/docs/robot1.jpeg",
  "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/docs/avocado.jpeg",
  "https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/docs/oranges.jpeg",
];

export function Preview() {
  const [verticalState, setVerticalState] = useState<ScrollShadowVisibility>("none");
  const [horizontalState, setHorizontalState] = useState<ScrollShadowVisibility>("none");

  const getRandomImage = (idx: number) => {
    return images[idx % images.length];
  };

  return (
    <div className="w-full sm:max-w-sm">
      <div className="mb-8 flex flex-col gap-2">
        <div className="rounded bg-default p-4">
          <p className="text-sm font-semibold">Vertical Shadow State: {verticalState}</p>
        </div>
        <div className="w-full">
          <ScrollShadow
            className="max-h-[240px] p-4"
            orientation="vertical"
            onVisibilityChange={(visibility) => setVerticalState(visibility)}
          >
            <div className="space-y-4">
              {Array.from({length: 10}).map((_, idx) => (
                <p key={`scroll-shadow-lorem-content-${idx}`}>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam pulvinar risus non
                  risus hendrerit venenatis. Pellentesque sit amet hendrerit risus, sed porttitor
                  quam. Morbi accumsan cursus enim, sed ultricies sapien.
                </p>
              ))}
            </div>
          </ScrollShadow>
        </div>
      </div>

      <div className="flex flex-col gap-2">
        <div className="rounded bg-default p-4">
          <p className="text-sm font-semibold">Horizontal Shadow State: {horizontalState}</p>
        </div>
        <div className="w-full">
          <ScrollShadow
            className="p-4"
            orientation="horizontal"
            onVisibilityChange={(visibility) => setHorizontalState(visibility)}
          >
            <div className="flex flex-row gap-4">
              {Array.from({length: 10}).map((_, idx) => (
                <Card
                  key={`scroll-shadow-lorem-cards-${idx}`}
                  className="flex min-w-[200px] flex-row gap-3 p-1"
                  variant="transparent"
                >
                  <img
                    alt="Lorem Card"
                    className="aspect-square h-16 w-16 shrink-0 rounded-xl object-cover select-none sm:h-20 sm:w-20"
                    loading="lazy"
                    src={getRandomImage(idx)}
                  />
                  <div className="flex flex-1 flex-col justify-center gap-1">
                    <Card.Title className="text-sm">Bridging the Future</Card.Title>
                    <Card.Description className="text-xs">Today, 6:30 PM</Card.Description>
                  </div>
                </Card>
              ))}
            </div>
          </ScrollShadow>
        </div>
      </div>
    </div>
  );
}
```
