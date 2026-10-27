# PromptInput

Cube component `PromptInput` from `@bosagent/cube-ui/prompt-input`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/prompt-input` |
| 分层 | Cube |
| 成熟度 | 代码可预览（@bosagent/cube-ui/prompt-input）。设计 registry 没有 PromptInput 规范条目。适用边界建设中。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/prompt-input` |

检索：PromptInput、prompt-input。

## Import

```tsx
import { PromptInput } from "@bosagent/cube-ui/prompt-input";
import { PromptInput } from "@bosagent/cube-ui";
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
| `allowSubmitWhileRunning` | `boolean` | No | `—` | — |
| `isDisabled` | `boolean` | No | `—` | — |
| `isPending` | `boolean` | No | `—` | — |
| `layout` | `PromptInputLayout` | No | `"stacked"` | Layout behavior for toolbar placement and inline resizing. |
| `lockInputOnRun` | `boolean` | No | `—` | — |
| `maxHeight` | `string \| number` | No | `—` | — |
| `onStop` | `() => void` | No | `—` | — |
| `onSubmit` | `() => void` | No | `—` | — |
| `onValueChange` | `(value: string) => void` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `status` | `ChatStatus` | No | `—` | — |
| `value` | `string` | No | `—` | — |
| `variant` | `PromptInputSurfaceVariant` | No | `"primary"` | Shell surface variant aligned with HeroUI OSS field inputs. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `PromptInput.Action`
- `PromptInput.Attachments`
- `PromptInput.Content`
- `PromptInput.Footer`
- `PromptInput.Queue`
- `PromptInput.Send`
- `PromptInput.Shell`
- `PromptInput.TextArea`
- `PromptInput.Token`
- `PromptInput.TokenInput`
- `PromptInput.TokenSuggestions`
- `PromptInput.Tokens`
- `PromptInput.Toolbar`
- `PromptInput.ToolbarEnd`
- `PromptInput.ToolbarStart`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

- [`--radius`](/foundations/theme)
- [`--field-border`](/foundations/theme)
- [`--border`](/foundations/theme)
- [`--field-background`](/foundations/theme)
- [`--default`](/foundations/theme)
- [`--field-border-hover`](/foundations/theme)
- [`--field-focus`](/foundations/theme)
- [`--field-border-focus`](/foundations/theme)
- [`--accent`](/foundations/theme)
- [`--accent-soft`](/foundations/theme)
- [`--accent-foreground`](/foundations/theme)
- [`--field-foreground`](/foundations/theme)
- [`--foreground`](/foundations/theme)
- [`--field-placeholder`](/foundations/theme)
- [`--muted`](/foundations/theme)
- [`--default-hover`](/foundations/theme)

从 packages/cube-ui/src/css/components/prompt-input.css 的 var() 引用抽出，且这些名字在 cube-contract.css 里存在。该文件还引用了 --ease-smooth 与 --ease-out，cube-contract.css 没有定义它们。未做逐项视觉验收。

## 画廊

[PromptInput](https://yuchuanux-a11y.github.io/cube-preview/#PromptInput)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/prompt-input.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { useState } from 'react';
import { ChatAttachmentInput } from '@components/chat-attachment';
import {
  PromptInput,
  TokenFieldValue,
  usePromptInputTokens,
} from '@components/prompt-input';
import { ArrowUp, Paperclip } from '@gravity-ui/icons';
import { Menu } from '@heroui/react';

export function Default() {
  const [value, setValue] = useState('');

  return (
    <div className="w-full max-w-[640px]">
      <PromptInput
        layout="inline"
        value={value}
        onSubmit={() => setValue('')}
        onValueChange={setValue}
      >
        <ChatAttachmentInput onFilesSelected={() => undefined}>
          <ChatAttachmentInput.Dropzone
            render={(dropzoneProps) => (
              <PromptInput.Shell {...dropzoneProps}>
                <PromptInput.Content>
                  <PromptInput.TextArea placeholder="What do you want to know?" />
                </PromptInput.Content>
                <PromptInput.Toolbar>
                  <PromptInput.ToolbarStart>
                    <ChatAttachmentInput.Trigger
                      render={(triggerProps) => (
                        <PromptInput.Action
                          {...triggerProps}
                          aria-label="Attach file"
                          tooltip="Attach file"
                        >
                          <Paperclip className="size-4" />
                        </PromptInput.Action>
                      )}
                    />
                  </PromptInput.ToolbarStart>
                  <PromptInput.ToolbarEnd>
                    <PromptInput.Send aria-label="Send">
                      <ArrowUp className="size-4" />
                    </PromptInput.Send>
                  </PromptInput.ToolbarEnd>
                </PromptInput.Toolbar>
              </PromptInput.Shell>
            )}
          />
        </ChatAttachmentInput>
        <PromptInput.Footer>
          AI can make mistakes. Check important info.
        </PromptInput.Footer>
      </PromptInput>
    </div>
  );
}

const mentionUsers = [
  { id: '1', name: 'Ada Lovelace', username: 'ada' },
  { id: '2', name: 'Grace Hopper', username: 'grace' },
  { id: '3', name: 'Alan Turing', username: 'alan' },
];

export function Tokens() {
  const tokens = usePromptInputTokens({ triggers: ['@'] });
  const items = mentionUsers.filter((user) =>
    user.username.startsWith(tokens.query)
  );

  return (
    <div className="w-full max-w-[640px]">
      <PromptInput onSubmit={() => tokens.setValue(new TokenFieldValue([]))}>
        <PromptInput.Shell>
          <PromptInput.Tokens>
            <PromptInput.Content>
              <PromptInput.TokenInput
                placeholder="Mention someone with @"
                tokens={tokens}
              />
            </PromptInput.Content>
            <PromptInput.TokenSuggestions tokens={tokens}>
              <Menu items={items}>
                {(item) => (
                  <Menu.Item
                    id={item.id}
                    onAction={() => tokens.insertToken(`@${item.username}`)}
                  >
                    {item.name}
                  </Menu.Item>
                )}
              </Menu>
            </PromptInput.TokenSuggestions>
          </PromptInput.Tokens>
          <PromptInput.Toolbar>
            <PromptInput.ToolbarEnd>
              <PromptInput.Send aria-label="Send">
                <ArrowUp className="size-4" />
              </PromptInput.Send>
            </PromptInput.ToolbarEnd>
          </PromptInput.Toolbar>
        </PromptInput.Shell>
      </PromptInput>
    </div>
  );
}
```
