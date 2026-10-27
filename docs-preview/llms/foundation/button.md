# Button

A clickable button component with multiple variants and states

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。规范 status 为 draft，Web implementation.status 为 prototype（docs/design-system/registry.json 与 examples/button.md）。设计验收未完成。 |
| 稳定 ID | `bos.component.button` |

检索：Button、button、bos.component.button、按钮、提交、主要操作、次要操作、危险操作、加载。

Native 目录说明：提供明确的操作入口与状态反馈。

中文检索词：按钮、提交、主要操作、次要操作、危险操作、加载。

## Import

```tsx
import { Button } from "@heroui/react";
```

## Preview

The docs page renders a live preview of the real component.

## 适用

来源：`docs/design-system/examples/button.md（草案，不是已发布规范）`。

- 用于提交或触发动作。
- 按动作后果写文案，例如“创建任务”“取消任务”，避免多个没有上下文的“确定”。
- 图标按钮需要可访问名称。

## 不适用

- 导航到地址时先选择语义正确的链接。
- 不要用本地计时器表示生产环境里的“创建成功”。等待真实结果。
- 不要在页面上另写一套主色、尺寸和动效。尺寸与 999px 圆角目前写在 cube-components.css，不是新的 token 别名。

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

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

- [`--accent`](/foundations/theme)
- [`--accent-foreground`](/foundations/theme)
- [`--accent-hover`](/foundations/theme)
- [`--accent-pressed`](/foundations/theme)
- [`--accent-disabled`](/foundations/theme)
- [`--accent-disabled-foreground`](/foundations/theme)
- [`--danger`](/foundations/theme)
- [`--danger-soft`](/foundations/theme)
- [`--danger-soft-foreground`](/foundations/theme)
- [`--danger-soft-hover`](/foundations/theme)
- [`--focus-inner`](/foundations/theme)
- [`--focus-outer`](/foundations/theme)
- [`--border-secondary`](/foundations/theme)
- [`--surface`](/foundations/theme)
- [`--foreground`](/foundations/theme)
- [`--default-hover`](/foundations/theme)
- [`--default-pressed`](/foundations/theme)
- [`--field-disabled`](/foundations/theme)
- [`--disabled-foreground`](/foundations/theme)
- [`--border`](/foundations/theme)

主操作使用 --accent / --accent-foreground。危险软按钮使用 --danger-soft。焦点使用 --focus-inner / --focus-outer。`.button` 的圆角是 cube-components.css 里的字面量 999px，高度是 32 / 40 / 48px，这些不是 cube-contract.css 的 token。

## Figma

[Open Button in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-69211)

## 画廊

[Button](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Button)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/button.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Button} from "@heroui/react";

export function Basic() {
  return <Button onPress={() => console.log("Button pressed")}>Click me</Button>;
}

export { Basic as Preview };
```
