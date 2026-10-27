# ChatMessage

Cube component `ChatMessage` from `@bosagent/cube-ui/chat-message`.

Cube component. Source: `packages/cube-ui/src/components/chat-message`.

## Import

```tsx
import { ChatMessage } from "@bosagent/cube-ui/chat-message";
import { ChatMessage } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props


### Action

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `aria-label` | `string` | No | `—` | Defines a string value that labels the current element. |
| `children` | `ReactNode` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `fullWidth` | `boolean` | No | `—` | — |
| `isIconOnly` | `boolean` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `tooltip` | `ReactNode` | No | `—` | — |
| `variant` | `"outline" \| "ghost" \| "danger" \| "danger-soft" \| "primary" \| "secondary" \| "tertiary"` | No | `—` | — |
| `aria-controls` | `string` | No | `—` | Identifies the element (or elements) whose contents or presence are controlled by the current element. |
| `aria-current` | `boolean \| "true" \| "false" \| "time" \| "page" \| "date" \| "step" \| "location"` | No | `—` | Indicates whether this element represents the current item within a container or set of related elements. |
| `aria-disabled` | `boolean \| "true" \| "false"` | No | `—` | Indicates whether the element is disabled to users of assistive technology. |
| `aria-expanded` | `boolean \| "true" \| "false"` | No | `—` | Indicates whether the element, or another grouping element it controls, is currently expanded or collapsed. |
| `aria-haspopup` | `boolean \| "true" \| "false" \| "dialog" \| "menu" \| "grid" \| "listbox" \| "tree"` | No | `—` | Indicates the availability and type of interactive popup element, such as menu or dialog, that can be triggered by an element. |
| `aria-pressed` | `boolean \| "true" \| "false" \| "mixed"` | No | `—` | Indicates the current "pressed" state of toggle buttons. |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `className` | `ClassNameOrFunction<ButtonRenderProps>` | No | `'react-aria-Button'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `form` | `string` | No | `—` | The `<form>` element to associate the button with. The value of this attribute must be the id of a `<form>` in the same document. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/button#form). |
| `formAction` | `string \| ((formData: FormData) => void \| Promise<void>)` | No | `—` | The URL that processes the information submitted by the button. Overrides the action attribute of the button's form owner. |
| `formEncType` | `string` | No | `—` | Indicates how to encode the form data that is submitted. |
| `formMethod` | `string` | No | `—` | Indicates the HTTP method used to submit the form. |
| `formNoValidate` | `boolean` | No | `—` | Indicates that the form is not to be validated when it is submitted. |

### Actions

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### Assistant

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### Avatar

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `alt` | `string` | Yes | `—` | — |
| `fallback` | `string` | No | `—` | — |
| `show` | `boolean` | No | `—` | — |
| `src` | `string` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### Body

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### Bubble

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### Content

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### Media

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

### User

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `ChatMessage.Action`
- `ChatMessage.Actions`
- `ChatMessage.Assistant`
- `ChatMessage.Avatar`
- `ChatMessage.Body`
- `ChatMessage.Bubble`
- `ChatMessage.Content`
- `ChatMessage.Media`
- `ChatMessage.User`

## Example source

```tsx
'use client';

import { ChatMessage } from '@components/chat-message';
import {
  ArrowsRotateLeft,
  Copy,
  ThumbsDown,
  ThumbsUp,
} from '@gravity-ui/icons';

export function Default() {
  return (
    <div className="mx-auto flex w-full max-w-[714px] flex-col gap-8">
      <ChatMessage.User>
        <ChatMessage.Bubble>
          <ChatMessage.Content>
            Can you explain how compound components help AI chat UIs stay
            SDK-agnostic?
          </ChatMessage.Content>
        </ChatMessage.Bubble>
      </ChatMessage.User>

      <ChatMessage.Assistant>
        <ChatMessage.Avatar show alt="Assistant" fallback="AI" />
        <ChatMessage.Body>
          <ChatMessage.Content>
            Compound components let you compose message layout explicitly while
            keeping state in your app layer.
          </ChatMessage.Content>
          <ChatMessage.Actions>
            <ChatMessage.Action aria-label="Copy" tooltip="Copy">
              <Copy className="size-4" />
            </ChatMessage.Action>
            <ChatMessage.Action
              aria-label="Good response"
              tooltip="Good response"
            >
              <ThumbsUp className="size-4" />
            </ChatMessage.Action>
            <ChatMessage.Action
              aria-label="Bad response"
              tooltip="Bad response"
            >
              <ThumbsDown className="size-4" />
            </ChatMessage.Action>
            <ChatMessage.Action aria-label="Regenerate" tooltip="Regenerate">
              <ArrowsRotateLeft className="size-4" />
            </ChatMessage.Action>
          </ChatMessage.Actions>
        </ChatMessage.Body>
      </ChatMessage.Assistant>
    </div>
  );
}
```
