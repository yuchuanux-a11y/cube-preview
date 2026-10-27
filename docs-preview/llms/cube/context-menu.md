# ContextMenu

Cube component `ContextMenu` from `@bosagent/cube-ui/context-menu`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/context-menu` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/context-menu` |

检索：ContextMenu、context-menu。

## Import

```tsx
import { ContextMenu } from "@bosagent/cube-ui/context-menu";
import { ContextMenu } from "@bosagent/cube-ui";
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
| `defaultOpen` | `boolean` | No | `—` | Default open state (uncontrolled). |
| `isDisabled` | `boolean` | No | `—` | Whether the context menu is disabled. |
| `onOpenChange` | `(open: boolean) => void` | No | `—` | Callback when open state changes. |
| `open` | `boolean` | No | `—` | Controlled open state. |

## Parts

- `ContextMenu.Item`
- `ContextMenu.ItemIndicator`
- `ContextMenu.Menu`
- `ContextMenu.Popover`
- `ContextMenu.Section`
- `ContextMenu.Separator`
- `ContextMenu.SubmenuIndicator`
- `ContextMenu.SubmenuTrigger`
- `ContextMenu.Trigger`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ContextMenu](https://yuchuanux-a11y.github.io/cube-preview/#ContextMenu)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/context-menu.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { ContextMenu } from '@components/context-menu';
import { Kbd, Label } from '@heroui/react';

export function Default() {
  return (
    <ContextMenu>
      <ContextMenu.Trigger>
        <div className="flex h-48 w-80 items-center justify-center rounded-xl border border-dashed border-border text-sm text-muted select-none">
          Right-click here
        </div>
      </ContextMenu.Trigger>
      <ContextMenu.Popover>
        <ContextMenu.Menu>
          <ContextMenu.Item id="back" textValue="Back">
            <Label>Back</Label>
            <Kbd className="ms-auto" slot="keyboard" variant="light">
              <Kbd.Abbr keyValue="command" />
              <Kbd.Content>[</Kbd.Content>
            </Kbd>
          </ContextMenu.Item>
          <ContextMenu.Item isDisabled id="forward" textValue="Forward">
            <Label>Forward</Label>
            <Kbd className="ms-auto" slot="keyboard" variant="light">
              <Kbd.Abbr keyValue="command" />
              <Kbd.Content>]</Kbd.Content>
            </Kbd>
          </ContextMenu.Item>
          <ContextMenu.Item id="reload" textValue="Reload">
            <Label>Reload</Label>
            <Kbd className="ms-auto" slot="keyboard" variant="light">
              <Kbd.Abbr keyValue="command" />
              <Kbd.Content>R</Kbd.Content>
            </Kbd>
          </ContextMenu.Item>
          <ContextMenu.Separator />
          <ContextMenu.Item id="view-source" textValue="View Page Source">
            <Label>View Page Source</Label>
          </ContextMenu.Item>
          <ContextMenu.Item id="inspect" textValue="Inspect">
            <Label>Inspect</Label>
          </ContextMenu.Item>
        </ContextMenu.Menu>
      </ContextMenu.Popover>
    </ContextMenu>
  );
}
```
