# Button

A clickable button component with multiple variants and states

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Button } from "@heroui/react";
```

## Figma

[Open Button in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-69211)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | No | `—` | — |
| `isIconOnly` | `boolean` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `variant` | `"outline" \| "ghost" \| "danger" \| "danger-soft" \| "primary" \| "secondary" \| "tertiary"` | No | `—` | — |
| `aria-controls` | `string` | No | `—` | Identifies the element (or elements) whose contents or presence are controlled by the current element. |
| `aria-current` | `boolean \| "true" \| "false" \| "time" \| "page" \| "date" \| "step" \| "location"` | No | `—` | Indicates whether this element represents the current item within a container or set of related elements. |
| `aria-disabled` | `boolean \| "true" \| "false"` | No | `—` | Indicates whether the element is disabled to users of assistive technology. |
| `aria-expanded` | `boolean \| "true" \| "false"` | No | `—` | Indicates whether the element, or another grouping element it controls, is currently expanded or collapsed. |
| `aria-haspopup` | `boolean \| "true" \| "false" \| "dialog" \| "menu" \| "grid" \| "listbox" \| "tree"` | No | `—` | Indicates the availability and type of interactive popup element, such as menu or dialog, that can be triggered by an element. |
| `aria-pressed` | `boolean \| "true" \| "false" \| "mixed"` | No | `—` | Indicates the current "pressed" state of toggle buttons. |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<ButtonRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ButtonRenderProps>` | No | `'react-aria-Button'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `form` | `string` | No | `—` | The `<form>` element to associate the button with. The value of this attribute must be the id of a `<form>` in the same document. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/button#form). |
| `formAction` | `string \| ((formData: FormData) => void \| Promise<void>)` | No | `—` | The URL that processes the information submitted by the button. Overrides the action attribute of the button's form owner. |
| `formEncType` | `string` | No | `—` | Indicates how to encode the form data that is submitted. |
| `formMethod` | `string` | No | `—` | Indicates the HTTP method used to submit the form. |
| `formNoValidate` | `boolean` | No | `—` | Indicates that the form is not to be validated when it is submitted. |
| `formTarget` | `string` | No | `—` | Overrides the target attribute of the button's form owner. |
| `isDisabled` | `boolean` | No | `—` | Whether the button is disabled. |
| `isPending` | `boolean` | No | `—` | Whether the button is in a pending state. This disables press and hover events while retaining focusability, and announces the pending state to screen readers. |
| `name` | `string` | No | `—` | Submitted as a pair with the button's value as part of the form data. |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onClick` | `(e: MouseEvent<FocusableElement>) => void` | No | `—` | **Not recommended – use `onPress` instead.** `onClick` is an alias for `onPress` provided for compatibility with other libraries. `onPress` provides additional event details for non-mouse interactions. |
| `onFocus` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `onHoverChange` | `(isHovering: boolean) => void` | No | `—` | Handler that is called when the hover state changes. |
| `onHoverEnd` | `(e: HoverEvent) => void` | No | `—` | Handler that is called when a hover interaction ends. |
| `onHoverStart` | `(e: HoverEvent) => void` | No | `—` | Handler that is called when a hover interaction starts. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is released. |
| `onPress` | `(e: PressEvent) => void` | No | `—` | Handler that is called when the press is released over the target. |
| `onPressChange` | `(isPressed: boolean) => void` | No | `—` | Handler that is called when the press state changes. |
| `onPressEnd` | `(e: PressEvent) => void` | No | `—` | Handler that is called when a press interaction ends, either over the target or when the pointer leaves the target. |
| `onPressStart` | `(e: PressEvent) => void` | No | `—` | Handler that is called when a press interaction starts. |
| `onPressUp` | `(e: PressEvent) => void` | No | `—` | Handler that is called when a press is released over the target, regardless of whether it started on the target or not. |
| `preventFocusOnPress` | `boolean` | No | `—` | Whether to prevent focus from moving to the button when pressing it. Caution, this can make the button inaccessible and should only be used when alternative keyboard interaction is provided, such as ComboBox's MenuTrigger or a NumberField's increment/decrement control. |
| `render` | `DOMRenderFunction<"button", ButtonRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ButtonRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `type` | `"button" \| "reset" \| "submit"` | No | `'button'` | The behavior of the button when used in an HTML form. |
| `value` | `string` | No | `—` | The value associated with the button's name when it's submitted with the form data. |

## Example source

```tsx
'use client';

import {Button} from "@heroui/react";

export function Basic() {
  return <Button onPress={() => console.log("Button pressed")}>Click me</Button>;
}

export { Basic as Preview };
```
