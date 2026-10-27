# Link

A styled anchor component for navigation with built-in icon support

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Link } from "@heroui/react";
```

## Figma

[Open Link in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-69635)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<LinkRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<LinkRenderProps>` | No | `'react-aria-Link'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `isDisabled` | `boolean` | No | `—` | Whether the link is disabled. |
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
| `render` | `(props: React.DetailedHTMLProps<React.HTMLAttributes<HTMLSpanElement>, HTMLSpanElement> \| React.DetailedHTMLProps<LinkWithRequiredHref, HTMLAnchorElement>, renderProps: LinkRender…` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Note: You can check if `'href' in props` in order to tell whether to render an `<a>` element. Requirements: - You must render the expected element type (e.g. if `<a>` is expected, you cannot render a `<button>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<LinkRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `Link.Icon`

## Example source

```tsx
'use client';

import {Link} from "@heroui/react";

export function LinkBasic() {
  return (
    <Link href="#">
      Call to action
      <Link.Icon />
    </Link>
  );
}

export { LinkBasic as Preview };
```
