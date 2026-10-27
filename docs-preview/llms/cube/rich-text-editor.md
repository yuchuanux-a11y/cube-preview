# RichTextEditor

Cube component `RichTextEditor` from `@bosagent/cube-ui/rich-text-editor`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/rich-text-editor` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/rich-text-editor` |

检索：RichTextEditor、rich-text-editor。

## Import

```tsx
import { RichTextEditor } from "@bosagent/cube-ui/rich-text-editor";
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
| `defaultValue` | `JSONContent` | No | `—` | — |
| `editorOptions` | `Partial<EditorOptions>` | No | `—` | — |
| `extensions` | `Extensions` | No | `—` | — |
| `isDisabled` | `boolean` | No | `—` | — |
| `isReadOnly` | `boolean` | No | `—` | — |
| `maxLength` | `number` | No | `—` | — |
| `onValueChange` | `(value: JSONContent, details: RichTextEditorValueChangeDetails) => void` | No | `—` | — |
| `placeholder` | `string` | No | `—` | — |
| `value` | `JSONContent` | No | `—` | — |
| `variant` | `RichTextEditorSurfaceVariant` | No | `"primary"` | Shell surface variant aligned with HeroUI OSS field inputs. |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `RichTextEditor.ActionButton`
- `RichTextEditor.BubbleMenu`
- `RichTextEditor.CharacterCount`
- `RichTextEditor.CommandButton`
- `RichTextEditor.Content`
- `RichTextEditor.FloatingMenu`
- `RichTextEditor.Footer`
- `RichTextEditor.LinkPopover`
- `RichTextEditor.Shell`
- `RichTextEditor.SuggestionMenu`
- `RichTextEditor.ToggleButton`
- `RichTextEditor.Toolbar`
- `RichTextEditor.ToolbarGroup`
- `RichTextEditor.ToolbarSeparator`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[RichTextEditor](https://yuchuanux-a11y.github.io/cube-preview/#RichTextEditor)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/rich-text-editor.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { RichTextEditor } from '@components/rich-text-editor';
import {
  ArrowShapeTurnUpLeft,
  ArrowShapeTurnUpRight,
  Bold,
  Code,
  Eraser,
  Heading1,
  Heading2,
  Italic,
  Link,
  ListUl,
  Strikethrough,
  Underline,
} from '@gravity-ui/icons';

const defaultValue = {
  content: [
    {
      content: [
        {
          text: 'Write a concise launch note for the beta 6 source sync.',
          type: 'text',
        },
      ],
      type: 'paragraph',
    },
  ],
  type: 'doc',
};

export function Default() {
  return (
    <RichTextEditor defaultValue={defaultValue} maxLength={1200}>
      <RichTextEditor.Shell>
        <RichTextEditor.Toolbar>
          <RichTextEditor.ToolbarGroup>
            <RichTextEditor.ActionButton action="undo" tooltip="Undo">
              <ArrowShapeTurnUpLeft className="size-4" />
            </RichTextEditor.ActionButton>
            <RichTextEditor.ActionButton action="redo" tooltip="Redo">
              <ArrowShapeTurnUpRight className="size-4" />
            </RichTextEditor.ActionButton>
          </RichTextEditor.ToolbarGroup>
          <RichTextEditor.ToolbarSeparator />
          <RichTextEditor.ToolbarGroup>
            <RichTextEditor.ToggleButton
              command="heading-1"
              tooltip="Heading 1"
            >
              <Heading1 className="size-4" />
            </RichTextEditor.ToggleButton>
            <RichTextEditor.ToggleButton
              command="heading-2"
              tooltip="Heading 2"
            >
              <Heading2 className="size-4" />
            </RichTextEditor.ToggleButton>
            <RichTextEditor.ToggleButton command="bold" tooltip="Bold">
              <Bold className="size-4" />
            </RichTextEditor.ToggleButton>
            <RichTextEditor.ToggleButton command="italic" tooltip="Italic">
              <Italic className="size-4" />
            </RichTextEditor.ToggleButton>
            <RichTextEditor.ToggleButton
              command="underline"
              tooltip="Underline"
            >
              <Underline className="size-4" />
            </RichTextEditor.ToggleButton>
            <RichTextEditor.ToggleButton command="strike" tooltip="Strike">
              <Strikethrough className="size-4" />
            </RichTextEditor.ToggleButton>
          </RichTextEditor.ToolbarGroup>
          <RichTextEditor.ToolbarSeparator />
          <RichTextEditor.ToolbarGroup>
            <RichTextEditor.ToggleButton command="bulletList" tooltip="Bullets">
              <ListUl className="size-4" />
            </RichTextEditor.ToggleButton>
            <RichTextEditor.ToggleButton
              command="codeBlock"
              tooltip="Code block"
            >
              <Code className="size-4" />
            </RichTextEditor.ToggleButton>
            <RichTextEditor.LinkPopover>
              <RichTextEditor.LinkPopover.Trigger aria-label="Link">
                <Link className="size-4" />
              </RichTextEditor.LinkPopover.Trigger>
              <RichTextEditor.LinkPopover.Content>
                <RichTextEditor.LinkPopover.Input />
                <RichTextEditor.LinkPopover.Actions>
                  <RichTextEditor.LinkPopover.UnsetButton />
                  <RichTextEditor.LinkPopover.ApplyButton />
                </RichTextEditor.LinkPopover.Actions>
              </RichTextEditor.LinkPopover.Content>
            </RichTextEditor.LinkPopover>
            <RichTextEditor.ActionButton
              action="clearFormatting"
              tooltip="Clear formatting"
            >
              <Eraser className="size-4" />
            </RichTextEditor.ActionButton>
          </RichTextEditor.ToolbarGroup>
        </RichTextEditor.Toolbar>
        <RichTextEditor.Content />
        <RichTextEditor.Footer>
          <span>Tip: select text to use the floating formatting toolbar.</span>
          <RichTextEditor.CharacterCount showWords />
        </RichTextEditor.Footer>
      </RichTextEditor.Shell>
      <RichTextEditor.BubbleMenu>
        <RichTextEditor.ToggleButton command="bold">
          <Bold className="size-4" />
        </RichTextEditor.ToggleButton>
        <RichTextEditor.ToggleButton command="italic">
          <Italic className="size-4" />
        </RichTextEditor.ToggleButton>
        <RichTextEditor.ToggleButton command="code">
          <Code className="size-4" />
        </RichTextEditor.ToggleButton>
      </RichTextEditor.BubbleMenu>
    </RichTextEditor>
  );
}
```
