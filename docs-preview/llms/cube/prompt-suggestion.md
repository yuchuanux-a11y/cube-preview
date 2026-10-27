# PromptSuggestion

Cube component `PromptSuggestion` from `@bosagent/cube-ui/prompt-suggestion`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/prompt-suggestion` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/prompt-suggestion` |

检索：PromptSuggestion、prompt-suggestion。

## Import

```tsx
import { PromptSuggestion } from "@bosagent/cube-ui/prompt-suggestion";
import { PromptSuggestion } from "@bosagent/cube-ui";
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
| `variant` | `"pill" \| "card"` | No | `"pill"` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `PromptSuggestion.Description`
- `PromptSuggestion.Group`
- `PromptSuggestion.Header`
- `PromptSuggestion.Item`
- `PromptSuggestion.ItemDescription`
- `PromptSuggestion.ItemFooter`
- `PromptSuggestion.ItemMeta`
- `PromptSuggestion.ItemTags`
- `PromptSuggestion.ItemTitle`
- `PromptSuggestion.Items`
- `PromptSuggestion.Title`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[PromptSuggestion](https://yuchuanux-a11y.github.io/cube-preview/#PromptSuggestion)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/prompt-suggestion.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { PromptSuggestion } from '@components/prompt-suggestion';

const SUGGESTED_PROMPTS = [
  'Draft a weekly project update email for my team',
  'Summarize this meeting transcript into action items',
  'Help me plan a product launch checklist',
  'Write a friendly reply to a customer support ticket',
  'Brainstorm names for a developer tools startup',
  'Explain this error message in plain language',
];

export function Default() {
  return (
    <div className="mx-auto w-full max-w-[714px]">
      <PromptSuggestion>
        <PromptSuggestion.Header>
          <PromptSuggestion.Title>
            What do you want to work on?
          </PromptSuggestion.Title>
          <PromptSuggestion.Description>
            Ask a question or start from one of the suggestions below.
          </PromptSuggestion.Description>
        </PromptSuggestion.Header>
        <PromptSuggestion.Items>
          {SUGGESTED_PROMPTS.map((prompt) => (
            <PromptSuggestion.Item key={prompt}>{prompt}</PromptSuggestion.Item>
          ))}
        </PromptSuggestion.Items>
      </PromptSuggestion>
    </div>
  );
}
```
