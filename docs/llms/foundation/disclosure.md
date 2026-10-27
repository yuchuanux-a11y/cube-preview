# Disclosure

A disclosure is a collapsible section with a header containing a heading and a trigger button, and a panel that wraps the content.

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Disclosure } from "@heroui/react";
```

## Figma

[Open Disclosure in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=6160-642)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ChildrenOrFunction<DisclosureRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<DisclosureRenderProps>` | No | `'react-aria-Disclosure'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultExpanded` | `boolean` | No | `—` | Whether the disclosure is expanded by default (uncontrolled). |
| `id` | `Key` | No | `—` | An id for the disclosure when used within a DisclosureGroup, matching the id used in `expandedKeys`. |
| `isDisabled` | `boolean` | No | `—` | Whether the disclosure is disabled. |
| `isExpanded` | `boolean` | No | `—` | Whether the disclosure is expanded (controlled). |
| `onExpandedChange` | `(isExpanded: boolean) => void` | No | `—` | Handler that is called when the disclosure's expanded state changes. |
| `render` | `DOMRenderFunction<"div", DisclosureRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<DisclosureRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `Disclosure.Body`
- `Disclosure.Content`
- `Disclosure.Heading`
- `Disclosure.Indicator`
- `Disclosure.Trigger`

## Example source

```tsx
'use client';

import {QrCode} from "@gravity-ui/icons";
import {Button, Disclosure} from "@heroui/react";
import React from "react";

export function Basic() {
  const [isExpanded, setIsExpanded] = React.useState(true);

  return (
    <div className="w-full max-w-md text-center">
      <Disclosure isExpanded={isExpanded} onExpandedChange={setIsExpanded}>
        <Disclosure.Heading>
          <Button slot="trigger" variant="secondary">
            <QrCode />
            Preview HeroUI Native
            <Disclosure.Indicator />
          </Button>
        </Disclosure.Heading>
        <Disclosure.Content>
          <Disclosure.Body className="shadow-panel flex flex-col items-center rounded-3xl bg-surface p-4 text-center">
            <p className="text-sm text-muted">
              Scan this QR code with your camera app to preview the HeroUI native components.
            </p>
            <img
              alt="Expo Go QR Code"
              className="aspect-square w-full max-w-54 object-cover"
              src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/images/qr-code-native.png"
            />
            <p className="text-sm text-muted">Expo must be installed on your device.</p>
            <Button className="mt-4" variant="primary">
              Download on App Store
            </Button>
          </Disclosure.Body>
        </Disclosure.Content>
      </Disclosure>
    </div>
  );
}

export { Basic as Preview };
```
