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

[`--radius`](/foundations/color) [`--field-border`](/foundations/color) [`--border`](/foundations/color) [`--field-background`](/foundations/color) [`--default`](/foundations/color) [`--field-border-hover`](/foundations/color) [`--field-focus`](/foundations/color) [`--field-border-focus`](/foundations/color) [`--accent`](/foundations/color) [`--accent-soft`](/foundations/color) [`--accent-foreground`](/foundations/color) [`--field-foreground`](/foundations/color) [`--foreground`](/foundations/color) [`--field-placeholder`](/foundations/color) [`--muted`](/foundations/color) [`--default-hover`](/foundations/color)

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#PromptInput
