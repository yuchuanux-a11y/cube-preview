# PromptInput

Cube component `PromptInput` from `@bosagent/cube-ui/prompt-input`.

- 分层：Cube
- 包：`@bosagent/cube-ui/prompt-input`
- 状态：建设中

## Import

```tsx
import { PromptInput } from "@bosagent/cube-ui/prompt-input";
import { PromptInput } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `allowSubmitWhileRunning` | `boolean` | 否 | `—` | — |
| `isDisabled` | `boolean` | 否 | `—` | — |
| `isPending` | `boolean` | 否 | `—` | — |
| `isReadOnly` | `boolean` | 否 | `—` | Keep the draft readable while preventing editing and submission. |
| `isUploading` | `boolean` | 否 | `—` | Host-owned upload state; blocks submission without reporting upload success. |
| `layout` | `PromptInputLayout` | 否 | `"stacked"` | Layout behavior for toolbar placement and inline resizing. |
| `lockInputOnRun` | `boolean` | 否 | `—` | — |
| `maxHeight` | `string \| number` | 否 | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | — |
| `status` | `ChatStatus` | 否 | `—` | — |
| `value` | `string` | 否 | `—` | — |
| `variant` | `PromptInputSurfaceVariant` | 否 | `"primary"` | Shell surface variant aligned with HeroUI OSS field inputs. |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onStop` | `() => void` | 否 | `—` | — |
| `onSubmit` | `() => void` | 否 | `—` | — |
| `onValueChange` | `(value: string) => void` | 否 | `—` | — |

</details>

## Parts

- `PromptInput.Action`
- `PromptInput.Attachments`
- `PromptInput.CardStack`
- `PromptInput.Content`
- `PromptInput.ContextTray`
- `PromptInput.Footer`
- `PromptInput.Queue`
- `PromptInput.QuickActions`
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

[`--accent`](#Docs/foundations/color) [`--accent-disabled`](#Docs/foundations/color) [`--accent-foreground`](#Docs/foundations/color) [`--accent-soft`](#Docs/foundations/color) [`--border-secondary`](#Docs/foundations/color) [`--default`](#Docs/foundations/color) [`--default-hover`](#Docs/foundations/color) [`--default-soft`](#Docs/foundations/color) [`--disabled-opacity`](#Docs/foundations/color) [`--field-background`](#Docs/foundations/color) [`--field-foreground`](#Docs/foundations/color) [`--field-placeholder`](#Docs/foundations/color) [`--focus-outer`](#Docs/foundations/color) [`--font-sans`](#Docs/foundations/color) [`--font-weight-normal`](#Docs/foundations/color) [`--foreground`](#Docs/foundations/color) [`--muted`](#Docs/foundations/color) [`--overlay`](#Docs/foundations/color) [`--radius`](#Docs/foundations/color) [`--radius-2xl`](#Docs/foundations/color) [`--radius-3xl`](#Docs/foundations/color) [`--radius-md`](#Docs/foundations/color) [`--radius-sm`](#Docs/foundations/color) [`--radius-xl`](#Docs/foundations/color) [`--spacing`](#Docs/foundations/color) [`--surface-secondary`](#Docs/foundations/color) [`--surface-shadow`](#Docs/foundations/color) [`--text-sm`](#Docs/foundations/color) [`--text-sm--line-height`](#Docs/foundations/color) [`--text-ui`](#Docs/foundations/color) [`--text-ui--line-height`](#Docs/foundations/color) [`--text-xs`](#Docs/foundations/color)

## 画廊

[Open in gallery](#PromptInput)
