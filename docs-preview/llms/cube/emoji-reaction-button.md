# EmojiReactionButton

Cube component `EmojiReactionButton` from `@bosagent/cube-ui/emoji-reaction-button`.

- 分层：Cube
- 包：`@bosagent/cube-ui/emoji-reaction-button`
- 状态：建设中

## Import

```tsx
import { EmojiReactionButton } from "@bosagent/cube-ui/emoji-reaction-button";
import { EmojiReactionButton } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `isReadOnly` | `boolean` | 否 | `—` | Whether the button is read-only and should not respond to user interaction. |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `"md"` | Size variant. |
| `autoFocus` | `boolean` | 否 | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<ToggleButtonRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ToggleButtonRenderProps>` | 否 | `'react-aria-ToggleButton'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultSelected` | `boolean` | 否 | `—` | Whether the element should be selected (uncontrolled). |
| `id` | `Key` | 否 | `—` | When used in a ToggleButtonGroup, an identifier for the item in `selectedKeys`. When used standalone, a DOM id. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the button is disabled. |
| `isSelected` | `boolean` | 否 | `—` | Whether the element should be selected (controlled). |
| `preventFocusOnPress` | `boolean` | 否 | `—` | Whether to prevent focus from moving to the button when pressing it. Caution, this can make the button inaccessible and should only be used when alternative keyboard interaction is provided, such as ComboBox's MenuTrigger or a NumberField's increment/decrement control. |
| `render` | `DOMRenderFunction<"button", ToggleButtonRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ToggleButtonRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `aria-controls` | `string` | 否 | `—` | Identifies the element (or elements) whose contents or presence are controlled by the current element. |
| `aria-disabled` | `boolean \| "true" \| "false"` | 否 | `—` | Indicates whether the element is disabled to users of assistive technology. |
| `aria-expanded` | `boolean \| "true" \| "false"` | 否 | `—` | Indicates whether the element, or another grouping element it controls, is currently expanded or collapsed. |
| `aria-haspopup` | `boolean \| "true" \| "false" \| "dialog" \| "menu" \| "grid" \| "listbox" \| "tree"` | 否 | `—` | Indicates the availability and type of interactive popup element, such as menu or dialog, that can be triggered by an element. |
| `aria-pressed` | `boolean \| "true" \| "false" \| "mixed"` | 否 | `—` | Indicates the current "pressed" state of toggle buttons. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(isSelected: boolean) => void` | 否 | `—` | Handler that is called when the element's selection state changes. |
| `onClick` | `(e: MouseEvent<FocusableElement>) => void` | 否 | `—` | **Not recommended – use `onPress` instead.** `onClick` is an alias for `onPress` provided for compatibility with other libraries. `onPress` provides additional event details for non-mouse interactions. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | 否 | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | 否 | `—` | Handler that is called when the element's focus status changes. |
| `onHoverChange` | `(isHovering: boolean) => void` | 否 | `—` | Handler that is called when the hover state changes. |
| `onHoverEnd` | `(e: HoverEvent) => void` | 否 | `—` | Handler that is called when a hover interaction ends. |
| `onHoverStart` | `(e: HoverEvent) => void` | 否 | `—` | Handler that is called when a hover interaction starts. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | 否 | `—` | Handler that is called when a key is released. |
| `onPress` | `(e: PressEvent) => void` | 否 | `—` | Handler that is called when the press is released over the target. |
| `onPressChange` | `(isPressed: boolean) => void` | 否 | `—` | Handler that is called when the press state changes. |
| `onPressEnd` | `(e: PressEvent) => void` | 否 | `—` | Handler that is called when a press interaction ends, either over the target or when the pointer leaves the target. |
| `onPressStart` | `(e: PressEvent) => void` | 否 | `—` | Handler that is called when a press interaction starts. |
| `onPressUp` | `(e: PressEvent) => void` | 否 | `—` | Handler that is called when a press is released over the target, regardless of whether it started on the target or not. |

</details>

## Parts

- `EmojiReactionButton.Count`
- `EmojiReactionButton.Emoji`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#EmojiReactionButton
