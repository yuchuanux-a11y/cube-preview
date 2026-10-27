# ErrorMessage

A low-level error message component for displaying errors

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { ErrorMessage } from "@heroui/react";
```

## Figma

[Open ErrorMessage in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17290-25455)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `elementType` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<any, any>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | — |

## Example source

```tsx
'use client';

import type {Key} from "@heroui/react";

import {Description, ErrorMessage, Label, Tag, TagGroup} from "@heroui/react";
import {useMemo, useState} from "react";

export function ErrorMessageBasic() {
  const [selected, setSelected] = useState<Iterable<Key>>(new Set());
  const isInvalid = useMemo(() => Array.from(selected).length === 0, [selected]);

  return (
    <TagGroup
      selectedKeys={selected}
      selectionMode="multiple"
      onSelectionChange={(keys) => setSelected(keys)}
    >
      <Label>Required Categories</Label>
      <TagGroup.List>
        <Tag id="news">News</Tag>
        <Tag id="travel">Travel</Tag>
        <Tag id="gaming">Gaming</Tag>
        <Tag id="shopping">Shopping</Tag>
      </TagGroup.List>
      <Description>Select at least one category</Description>
      <ErrorMessage>{!!isInvalid && <>Please select at least one category</>}</ErrorMessage>
    </TagGroup>
  );
}

export { ErrorMessageBasic as Preview };
```
