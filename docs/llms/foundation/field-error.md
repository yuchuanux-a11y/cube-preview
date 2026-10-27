# FieldError

Displays validation error messages for form fields

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { FieldError } from "@heroui/react";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ChildrenOrFunction<FieldErrorRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<FieldErrorRenderProps>` | No | `'react-aria-FieldError'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `elementType` | `string` | No | `'span'` | The HTML element type to render. Defaults to `'span'`. Set to `'div'` when using block-level children (e.g. `<ul>`) to avoid invalid HTML. |
| `render` | `DOMRenderFunction<"div", FieldErrorRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `style` | `StyleOrFunction<FieldErrorRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Example source

```tsx
'use client';

import {FieldError, Input, Label, TextField} from "@heroui/react";
import {useState} from "react";

export function Basic() {
  const [value, setValue] = useState("jr");
  const isInvalid = value.length > 0 && value.length < 3;

  return (
    <TextField className="w-64" isInvalid={isInvalid}>
      <Label htmlFor="username">Username</Label>
      <Input
        id="username"
        placeholder="Enter username"
        value={value}
        onChange={(e) => setValue(e.target.value)}
      />
      <FieldError>Username must be at least 3 characters</FieldError>
    </TextField>
  );
}

export { Basic as Preview };
```
