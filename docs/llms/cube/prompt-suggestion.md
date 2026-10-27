# PromptSuggestion

Cube component `PromptSuggestion` from `@bosagent/cube-ui/prompt-suggestion`.

Cube component. Source: `packages/cube-ui/src/components/prompt-suggestion`.

## Import

```tsx
import { PromptSuggestion } from "@bosagent/cube-ui/prompt-suggestion";
import { PromptSuggestion } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
