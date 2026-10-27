# PromptInput

Cube component `PromptInput` from `@bosagent/cube-ui/prompt-input`.

Cube component. Source: `packages/cube-ui/src/components/prompt-input`.

## Import

```tsx
import { PromptInput } from "@bosagent/cube-ui/prompt-input";
import { PromptInput } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
