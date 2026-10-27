# HoverCard

Cube component `HoverCard` from `@bosagent/cube-ui/hover-card`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/hover-card` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/hover-card` |

检索：HoverCard、hover-card。

## Import

```tsx
import { HoverCard } from "@bosagent/cube-ui/hover-card";
import { HoverCard } from "@bosagent/cube-ui";
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
| `closeDelay` | `number` | No | `300` | Time in ms before the hover card closes after pointer/focus leave. |
| `defaultOpen` | `boolean` | No | `—` | Default open state (uncontrolled). |
| `isDisabled` | `boolean` | No | `—` | Whether the hover card is disabled and never opens. |
| `onOpenChange` | `(open: boolean) => void` | No | `—` | Callback when open state changes. |
| `open` | `boolean` | No | `—` | Controlled open state. |
| `openDelay` | `number` | No | `700` | Time in ms before the hover card opens after hover. |

## Parts

- `HoverCard.Arrow`
- `HoverCard.Content`
- `HoverCard.Trigger`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[HoverCard](https://yuchuanux-a11y.github.io/cube-preview/#HoverCard)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/hover-card.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { HoverCard } from '@components/hover-card';
import { Avatar, Link } from '@heroui/react';

export function Default() {
  return (
    <div className="px-10 py-24">
      <p className="text-sm leading-8">
        Check out{' '}
        <HoverCard>
          <HoverCard.Trigger>
            <Link
              className="underline"
              href="https://x.com/hero_ui"
              target="_blank"
            >
              @hero_ui
            </Link>
          </HoverCard.Trigger>
          <HoverCard.Content>
            <div className="flex items-center gap-3">
              <Avatar size="sm">
                <Avatar.Image
                  alt="HeroUI"
                  src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/docs/heroui_isotipo.png"
                />
                <Avatar.Fallback>H</Avatar.Fallback>
              </Avatar>
              <div className="flex flex-col items-start justify-center">
                <span className="text-sm leading-4 font-semibold">HeroUI</span>
                <span className="text-sm tracking-tight text-muted">
                  @hero_ui
                </span>
              </div>
            </div>
            <p className="mt-3 pl-px text-sm font-medium">
              Building the future of UI for web & mobile.&nbsp;
              <br />
              <span aria-label="confetti" role="img">
                🚀
              </span>
              &nbsp;(YC S24)&nbsp;
            </p>
            <div className="mt-3 flex gap-2">
              <div className="flex gap-1">
                <p className="text-sm font-semibold">4</p>
                <p className="text-sm text-muted">Following</p>
              </div>
              <div className="flex gap-1">
                <p className="text-sm font-semibold">97.1K</p>
                <p className="text-sm text-muted">Followers</p>
              </div>
            </div>
          </HoverCard.Content>
        </HoverCard>{' '}
        for beautiful React components.
      </p>
    </div>
  );
}
```
