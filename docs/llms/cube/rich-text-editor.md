# RichTextEditor

Cube component `RichTextEditor` from `@bosagent/cube-ui/rich-text-editor`.

Cube component. Source: `packages/cube-ui/src/components/rich-text-editor`.

## Import

```tsx
import { RichTextEditor } from "@bosagent/cube-ui/rich-text-editor";
```

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
