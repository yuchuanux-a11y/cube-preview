# ChatAttachment

Cube component `ChatAttachment` from `@bosagent/cube-ui/chat-attachment`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/chat-attachment` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/chat-attachment` |

检索：ChatAttachment、chat-attachment。

## Import

```tsx
import { ChatAttachment } from "@bosagent/cube-ui/chat-attachment";
import { ChatAttachment } from "@bosagent/cube-ui";
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
| `children` | `React.ReactNode` | No | `—` | — |
| `mediaType` | `ChatAttachmentMediaType` | No | `—` | — |
| `mimeType` | `string` | No | `—` | — |
| `name` | `string` | No | `—` | — |
| `size` | `number` | No | `—` | — |
| `src` | `string` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `ChatAttachment.Icon`
- `ChatAttachment.Info`
- `ChatAttachment.Name`
- `ChatAttachment.Preview`
- `ChatAttachment.Remove`
- `ChatAttachment.Size`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ChatAttachment](https://yuchuanux-a11y.github.io/cube-preview/#ChatAttachment)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/chat-attachment.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { useEffect, useRef, useState } from 'react';
import {
  ChatAttachment,
  ChatAttachmentGroup,
  ChatAttachmentInput,
} from '@components/chat-attachment';
import { ChatMessage } from '@components/chat-message';
import { PromptInput } from '@components/prompt-input';
import { ArrowUp, Paperclip } from '@gravity-ui/icons';

type PendingAttachment = {
  id: string;
  name: string;
  size?: number;
  src?: string;
  mimeType?: string;
};

function createAttachmentId(file: File): string {
  return `${file.name}-${file.lastModified}-${
    globalThis.crypto?.randomUUID?.() ?? Math.random().toString(36).slice(2)
  }`;
}

function revokeAttachmentUrl(attachment: PendingAttachment) {
  if (attachment.src?.startsWith('blob:')) URL.revokeObjectURL(attachment.src);
}

function revokeAttachmentUrls(attachments: readonly PendingAttachment[]) {
  attachments.forEach(revokeAttachmentUrl);
}

export function Default() {
  return (
    <ChatMessage.User>
      <ChatAttachmentGroup className="mb-2">
        <ChatAttachment
          mediaType="image"
          name="screenshot.png"
          src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/images/egg.webp"
        />
      </ChatAttachmentGroup>
      <ChatMessage.Bubble>
        <ChatMessage.Content>What is in this screenshot?</ChatMessage.Content>
      </ChatMessage.Bubble>
    </ChatMessage.User>
  );
}

export function Composer() {
  const [attachments, setAttachments] = useState<PendingAttachment[]>([]);
  const attachmentsRef = useRef<PendingAttachment[]>([]);

  useEffect(() => {
    attachmentsRef.current = attachments;
  }, [attachments]);

  useEffect(() => {
    return () => revokeAttachmentUrls(attachmentsRef.current);
  }, []);

  const handleFilesSelected = (files: File[]) => {
    setAttachments((current) => [
      ...current,
      ...files.map((file) => ({
        id: createAttachmentId(file),
        mimeType: file.type,
        name: file.name,
        size: file.size,
        src:
          file.type.startsWith('image/') || file.type.startsWith('video/')
            ? URL.createObjectURL(file)
            : undefined,
      })),
    ]);
  };

  return (
    <PromptInput className="max-w-xl">
      <ChatAttachmentInput
        accept="image/*,.pdf"
        onFilesSelected={handleFilesSelected}
      >
        <ChatAttachmentInput.Dropzone
          render={(dropzoneProps) => (
            <PromptInput.Shell {...dropzoneProps}>
              <PromptInput.Content>
                {attachments.length ? (
                  <PromptInput.Attachments>
                    <ChatAttachmentGroup>
                      {attachments.map((file) => (
                        <ChatAttachment
                          key={file.id}
                          mimeType={file.mimeType}
                          name={file.name}
                          size={file.size}
                          src={file.src}
                        >
                          <ChatAttachment.Preview />
                          <ChatAttachment.Info />
                          <ChatAttachment.Remove
                            aria-label="Remove attachment"
                            onPress={() =>
                              setAttachments((current) => {
                                const removed = current.find(
                                  (item) => item.id === file.id
                                );

                                if (removed) revokeAttachmentUrl(removed);

                                return current.filter(
                                  (item) => item.id !== file.id
                                );
                              })
                            }
                          />
                        </ChatAttachment>
                      ))}
                    </ChatAttachmentGroup>
                  </PromptInput.Attachments>
                ) : null}
                <PromptInput.TextArea placeholder="Ask about your files..." />
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
    </PromptInput>
  );
}

export function Grouped() {
  return (
    <ChatAttachmentGroup>
      <ChatAttachment
        mimeType="application/pdf"
        name="brief.pdf"
        size={248_320}
      />
      <ChatAttachment
        mimeType="application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
        name="budget.xlsx"
        size={1_048_576}
      />
      <ChatAttachment
        mediaType="image"
        name="wireframe.png"
        size={512_000}
        src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/images/egg.webp"
      />
      <ChatAttachment
        mediaType="image"
        name="screenshot.png"
        src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/images/egg.webp"
      />
    </ChatAttachmentGroup>
  );
}
```
