# RichTextEditor

Cube component `RichTextEditor` from `@bosagent/cube-ui/rich-text-editor`.

- 分层：Cube
- 包：`@bosagent/cube-ui/rich-text-editor`
- 状态：建设中

## Import

```tsx
import { RichTextEditor } from "@bosagent/cube-ui/rich-text-editor";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `defaultValue` | `JSONContent` | 否 | `—` | — |
| `editorOptions` | `Partial<EditorOptions>` | 否 | `—` | — |
| `extensions` | `Extensions` | 否 | `—` | — |
| `isDisabled` | `boolean` | 否 | `—` | — |
| `isReadOnly` | `boolean` | 否 | `—` | — |
| `maxLength` | `number` | 否 | `—` | — |
| `placeholder` | `string` | 否 | `—` | — |
| `value` | `JSONContent` | 否 | `—` | — |
| `variant` | `RichTextEditorSurfaceVariant` | 否 | `"primary"` | Shell surface variant aligned with HeroUI OSS field inputs. |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onValueChange` | `(value: JSONContent, details: RichTextEditorValueChangeDetails) => void` | 否 | `—` | — |

</details>

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

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#RichTextEditor
