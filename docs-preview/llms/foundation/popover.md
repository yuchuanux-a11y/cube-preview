# Popover

Displays rich content in a portal triggered by a button or any custom element

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：Popover、popover。

Native 目录说明：在触发位置附近显示补充内容。

## Import

```tsx
import { Popover } from "@heroui/react";
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
| `children` | `React.ReactNode` | Yes | `—` | — |
| `defaultOpen` | `boolean` | No | `—` | Whether the overlay is open by default (uncontrolled). |
| `isOpen` | `boolean` | No | `—` | Whether the overlay is open by default (controlled). |
| `onOpenChange` | `(isOpen: boolean) => void` | No | `—` | Handler that is called when the overlay's open state changes. |

## Parts

- `Popover.Arrow`
- `Popover.Content`
- `Popover.Dialog`
- `Popover.Heading`
- `Popover.Trigger`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open Popover in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=6192-4931)

## 画廊

[Popover](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Popover)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/popover.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Avatar, Button, Popover} from "@heroui/react";
import {useState} from "react";

export function PopoverInteractive() {
  const [isFollowing, setIsFollowing] = useState(false);

  return (
    <div className="flex items-center gap-6">
      <Popover>
        <Popover.Trigger aria-label="User profile">
          <div className="flex items-center gap-2">
            <Avatar size="sm">
              <Avatar.Image
                alt="Sarah Johnson"
                src="https://img.heroui.chat/image/avatar?w=400&h=400&u=1"
              />
              <Avatar.Fallback>SJ</Avatar.Fallback>
            </Avatar>
            <div className="flex flex-col">
              <p className="text-sm font-medium">Sarah Johnson</p>
              <p className="text-xs text-muted">@sarahj</p>
            </div>
          </div>
        </Popover.Trigger>
        <Popover.Content className="w-[320px]">
          <Popover.Dialog>
            <Popover.Heading>
              <div className="flex items-center justify-between">
                <div className="flex items-center gap-3">
                  <Avatar size="md">
                    <Avatar.Image
                      alt="Sarah Johnson"
                      src="https://img.heroui.chat/image/avatar?w=400&h=400&u=1"
                    />
                    <Avatar.Fallback>SJ</Avatar.Fallback>
                  </Avatar>
                  <div>
                    <p className="font-semibold">Sarah Johnson</p>
                    <p className="text-sm text-muted">@sarahj</p>
                  </div>
                </div>
                <Button
                  className="rounded-full"
                  size="sm"
                  variant={isFollowing ? "tertiary" : "primary"}
                  onPress={() => setIsFollowing(!isFollowing)}
                >
                  {isFollowing ? "Following" : "Follow"}
                </Button>
              </div>
            </Popover.Heading>
            <p className="mt-3 text-sm text-muted">
              Product designer and creative director. Building beautiful experiences that matter.
            </p>
            <div className="mt-3 flex gap-4">
              <div>
                <span className="font-semibold">892</span>
                <span className="ms-1 text-sm text-muted">Following</span>
              </div>
              <div>
                <span className="font-semibold">12.5K</span>
                <span className="ms-1 text-sm text-muted">Followers</span>
              </div>
            </div>
          </Popover.Dialog>
        </Popover.Content>
      </Popover>
    </div>
  );
}

export { PopoverInteractive as Preview };
```
