# ChatMessage

Cube component `ChatMessage` from `@bosagent/cube-ui/chat-message`.

- 分层：Cube
- 包：`@bosagent/cube-ui/chat-message`
- 状态：建设中

## Import

```tsx
import { ChatMessage } from "@bosagent/cube-ui/chat-message";
import { ChatMessage } from "@bosagent/cube-ui";
```

## Props


### Action

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `aria-label` | `string` | 否 | `—` | Defines a string value that labels the current element. |
| `children` | `ReactNode` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `fullWidth` | `boolean` | 否 | `—` | — |
| `isIconOnly` | `boolean` | 否 | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | — |
| `tooltip` | `ReactNode` | 否 | `—` | — |
| `variant` | `"outline" \| "ghost" \| "danger" \| "danger-soft" \| "primary" \| "secondary" \| "tertiary"` | 否 | `—` | — |
| `aria-controls` | `string` | 否 | `—` | Identifies the element (or elements) whose contents or presence are controlled by the current element. |
| `aria-current` | `boolean \| "true" \| "false" \| "time" \| "page" \| "date" \| "step" \| "location"` | 否 | `—` | Indicates whether this element represents the current item within a container or set of related elements. |
| `aria-disabled` | `boolean \| "true" \| "false"` | 否 | `—` | Indicates whether the element is disabled to users of assistive technology. |
| `aria-expanded` | `boolean \| "true" \| "false"` | 否 | `—` | Indicates whether the element, or another grouping element it controls, is currently expanded or collapsed. |
| `aria-haspopup` | `boolean \| "true" \| "false" \| "dialog" \| "menu" \| "grid" \| "listbox" \| "tree"` | 否 | `—` | Indicates the availability and type of interactive popup element, such as menu or dialog, that can be triggered by an element. |
| `aria-pressed` | `boolean \| "true" \| "false" \| "mixed"` | 否 | `—` | Indicates the current "pressed" state of toggle buttons. |
| `autoFocus` | `boolean` | 否 | `—` | Whether the element should receive focus on render. |
| `className` | `ClassNameOrFunction<ButtonRenderProps>` | 否 | `'react-aria-Button'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `form` | `string` | 否 | `—` | The `<form>` element to associate the button with. The value of this attribute must be the id of a `<form>` in the same document. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/button#form). |
| `formAction` | `string \| ((formData: FormData) => void \| Promise<void>)` | 否 | `—` | The URL that processes the information submitted by the button. Overrides the action attribute of the button's form owner. |
| `formEncType` | `string` | 否 | `—` | Indicates how to encode the form data that is submitted. |
| `formMethod` | `string` | 否 | `—` | Indicates the HTTP method used to submit the form. |
| `formNoValidate` | `boolean` | 否 | `—` | Indicates that the form is not to be validated when it is submitted. |

### Actions

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

### Assistant

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

### Avatar

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `alt` | `string` | 是 | `—` | — |
| `fallback` | `string` | 否 | `—` | — |
| `show` | `boolean` | 否 | `—` | — |
| `src` | `string` | 否 | `—` | — |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

### Body

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

### Bubble

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

### Content

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

### Media

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

### User

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

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

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#ChatMessage
