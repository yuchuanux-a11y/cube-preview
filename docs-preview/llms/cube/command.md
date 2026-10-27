# Command

Cube component `Command` from `@bosagent/cube-ui/command`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/command` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/command` |

检索：Command、command。

## Import

```tsx
import { Command } from "@bosagent/cube-ui/command";
import { Command } from "@bosagent/cube-ui";
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

## Parts

- `Command.Backdrop`
- `Command.Container`
- `Command.Dialog`
- `Command.Footer`
- `Command.Group`
- `Command.Header`
- `Command.InputGroup`
- `Command.Item`
- `Command.List`
- `Command.Separator`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[Command](https://yuchuanux-a11y.github.io/cube-preview/#Command)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/command.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { useState } from 'react';
import { Command } from '@components/command';
import {
  FilePlus,
  FolderPlus,
  Keyboard,
  Magnifier,
  Palette,
  PersonNutHex,
  PersonPencil,
} from '@gravity-ui/icons';
import { Button, Chip, Kbd } from '@heroui/react';

export function Default() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <>
      <Button variant="outline" onPress={() => setIsOpen(true)}>
        Open Command Palette{' '}
        <Kbd>
          <Kbd.Abbr keyValue="command" />
          <Kbd.Content>K</Kbd.Content>
        </Kbd>
      </Button>
      <Command>
        <Command.Backdrop isOpen={isOpen} onOpenChange={setIsOpen}>
          <Command.Container>
            <Command.Dialog>
              <Command.Header>
                <Chip size="sm">Home</Chip>
              </Command.Header>
              <Command.InputGroup>
                <Command.InputGroup.Prefix>
                  <Magnifier />
                </Command.InputGroup.Prefix>
                <Command.InputGroup.Input placeholder="Type a command or search..." />
                <Command.InputGroup.ClearButton />
                <Command.InputGroup.Suffix>
                  <Kbd className="text-xs">
                    <Kbd.Content>Esc</Kbd.Content>
                  </Kbd>
                </Command.InputGroup.Suffix>
              </Command.InputGroup>
              <Command.List>
                <Command.Group heading="Actions">
                  <Command.Item textValue="Create new file">
                    <FilePlus />
                    <span>Create new file...</span>
                  </Command.Item>
                  <Command.Item textValue="Create new folder">
                    <FolderPlus />
                    <span>Create new folder...</span>
                  </Command.Item>
                  <Command.Item textValue="Assign to me">
                    <PersonPencil />
                    <span>Assign to me</span>
                  </Command.Item>
                </Command.Group>
                <Command.Group heading="Settings">
                  <Command.Item textValue="Preferences">
                    <PersonNutHex />
                    <span>Preferences</span>
                  </Command.Item>
                  <Command.Item textValue="Change theme">
                    <Palette />
                    <span>Change theme</span>
                  </Command.Item>
                  <Command.Item textValue="Keyboard shortcuts">
                    <Keyboard />
                    <span>Keyboard shortcuts</span>
                  </Command.Item>
                </Command.Group>
              </Command.List>
              <Command.Footer className="justify-between [&_kbd]:h-5 [&_kbd]:text-xs">
                <div className="flex items-center gap-3">
                  <div className="flex items-center gap-2">
                    <div className="flex items-center gap-0.5">
                      <Kbd className="text-xs">
                        <Kbd.Abbr keyValue="up" />
                      </Kbd>
                      <Kbd className="text-xs">
                        <Kbd.Abbr keyValue="down" />
                      </Kbd>
                    </div>
                    <span>Navigate</span>
                  </div>
                  <div className="flex items-center gap-2">
                    <Kbd>
                      <Kbd.Abbr keyValue="enter" />
                    </Kbd>
                    <span>Select</span>
                  </div>
                </div>
              </Command.Footer>
            </Command.Dialog>
          </Command.Container>
        </Command.Backdrop>
      </Command>
    </>
  );
}
```
