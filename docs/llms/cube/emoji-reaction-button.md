# EmojiReactionButton

Cube component `EmojiReactionButton` from `@bosagent/cube-ui/emoji-reaction-button`.

Cube component. Source: `packages/cube-ui/src/components/emoji-reaction-button`.

## Import

```tsx
import { EmojiReactionButton } from "@bosagent/cube-ui/emoji-reaction-button";
import { EmojiReactionButton } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `isReadOnly` | `boolean` | No | `—` | Whether the button is read-only and should not respond to user interaction. |
| `size` | `"md" \| "lg" \| "sm"` | No | `"md"` | Size variant. |
| `aria-controls` | `string` | No | `—` | Identifies the element (or elements) whose contents or presence are controlled by the current element. |
| `aria-disabled` | `boolean \| "true" \| "false"` | No | `—` | Indicates whether the element is disabled to users of assistive technology. |
| `aria-expanded` | `boolean \| "true" \| "false"` | No | `—` | Indicates whether the element, or another grouping element it controls, is currently expanded or collapsed. |
| `aria-haspopup` | `boolean \| "true" \| "false" \| "dialog" \| "menu" \| "grid" \| "listbox" \| "tree"` | No | `—` | Indicates the availability and type of interactive popup element, such as menu or dialog, that can be triggered by an element. |
| `aria-pressed` | `boolean \| "true" \| "false" \| "mixed"` | No | `—` | Indicates the current "pressed" state of toggle buttons. |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<ToggleButtonRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ToggleButtonRenderProps>` | No | `'react-aria-ToggleButton'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultSelected` | `boolean` | No | `—` | Whether the element should be selected (uncontrolled). |
| `id` | `Key` | No | `—` | When used in a ToggleButtonGroup, an identifier for the item in `selectedKeys`. When used standalone, a DOM id. |
| `isDisabled` | `boolean` | No | `—` | Whether the button is disabled. |
| `isSelected` | `boolean` | No | `—` | Whether the element should be selected (controlled). |
| `onBlur` | `(e: FocusEvent<Element, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(isSelected: boolean) => void` | No | `—` | Handler that is called when the element's selection state changes. |
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
| `render` | `DOMRenderFunction<"button", ToggleButtonRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ToggleButtonRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `EmojiReactionButton.Count`
- `EmojiReactionButton.Emoji`

## Example source

```tsx
'use client';

import { useState } from 'react';
import { EmojiReactionButton } from '@components/emoji-reaction-button';

export function Default() {
  const [reactions, setReactions] = useState<
    Record<string, { count: number; selected: boolean }>
  >({
    '❤️': { count: 12, selected: true },
    '🎉': { count: 1, selected: false },
    '👍': { count: 5, selected: false },
    '😂': { count: 3, selected: false },
    '🚀': { count: 1, selected: false },
  });

  const toggle = (emoji: string) => {
    setReactions((prev) => {
      const reaction = prev[emoji];

      if (!reaction) return prev;
      const selected = !reaction.selected;
      const count = selected ? reaction.count + 1 : reaction.count - 1;

      if (count < 1) {
        const { [emoji]: _, ...rest } = prev;

        return rest;
      }

      return { ...prev, [emoji]: { count, selected } };
    });
  };

  return (
    <div className="flex flex-wrap items-center gap-2">
      {Object.entries(reactions).map(([emoji, { count, selected }]) => (
        <EmojiReactionButton
          key={emoji}
          isSelected={selected}
          onChange={() => toggle(emoji)}
        >
          <EmojiReactionButton.Emoji>{emoji}</EmojiReactionButton.Emoji>
          {count > 0 && (
            <EmojiReactionButton.Count>{count}</EmojiReactionButton.Count>
          )}
        </EmojiReactionButton>
      ))}
    </div>
  );
}
```
