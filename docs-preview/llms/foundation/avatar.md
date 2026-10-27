# Avatar

Display user profile images with customizable fallback content

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：Avatar、avatar。

Native 目录说明：以图片或文字标识团队成员。

## Import

```tsx
import { Avatar } from "@heroui/react";
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
| `color` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `variant` | `"default" \| "soft"` | No | `—` | — |
| `asChild` | `boolean` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `Avatar.Fallback`
- `Avatar.Image`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open Avatar in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-71386)

## 画廊

[Avatar](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Avatar)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/avatar.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Avatar} from "@heroui/react";

export function Basic() {
  return (
    <div className="flex items-center gap-4">
      <Avatar>
        <Avatar.Image alt="John Doe" src="https://img.heroui.chat/image/avatar?w=400&h=400&u=3" />
        <Avatar.Fallback>JD</Avatar.Fallback>
      </Avatar>
      <Avatar>
        <Avatar.Image
          alt="Blue"
          src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/avatars/blue.jpg"
        />
        <Avatar.Fallback>B</Avatar.Fallback>
      </Avatar>
      <Avatar>
        <Avatar.Fallback>JR</Avatar.Fallback>
      </Avatar>
    </div>
  );
}

export { Basic as Preview };
```
