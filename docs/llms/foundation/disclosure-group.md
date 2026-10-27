# DisclosureGroup

Container that manages multiple Disclosure items with coordinated expanded states

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { DisclosureGroup } from "@heroui/react";
```

## Figma

[Open DisclosureGroup in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-43646)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `allowsMultipleExpanded` | `boolean` | No | `—` | Whether multiple items can be expanded at the same time. |
| `children` | `ChildrenOrFunction<DisclosureGroupRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<DisclosureGroupRenderProps>` | No | `'react-aria-DisclosureGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultExpandedKeys` | `Iterable<Key>` | No | `—` | The initial expanded keys in the group (uncontrolled). |
| `expandedKeys` | `Iterable<Key>` | No | `—` | The currently expanded keys in the group (controlled). |
| `isDisabled` | `boolean` | No | `—` | Whether all items are disabled. |
| `onExpandedChange` | `(keys: Set<Key>) => any` | No | `—` | Handler that is called when items are expanded or collapsed. |
| `render` | `DOMRenderFunction<"div", DisclosureGroupRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `style` | `StyleOrFunction<DisclosureGroupRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Example source

```tsx
'use client';

import {QrCode} from "@gravity-ui/icons";
import {Button, cn, Disclosure, DisclosureGroup, Separator} from "@heroui/react";
import React from "react";

export function Basic() {
  const [expandedKeys, setExpandedKeys] = React.useState(new Set<string | number>(["preview"]));

  return (
    <div className="w-full max-w-md">
      <div className="flex flex-col gap-4 bg-transparent p-4">
        <DisclosureGroup expandedKeys={expandedKeys} onExpandedChange={setExpandedKeys}>
          <Disclosure aria-label="Preview HeroUI Native" id="preview">
            <Disclosure.Heading>
              <Button
                slot="trigger"
                variant={expandedKeys.has("preview") ? "secondary" : "tertiary"}
                className={cn("w-full border-none", {
                  "bg-transparent": !expandedKeys.has("preview"),
                })}
              >
                <div className="flex w-full items-center justify-start gap-2">
                  <QrCode />
                  Preview HeroUI Native
                </div>
                <Disclosure.Indicator className="text-muted" />
              </Button>
            </Disclosure.Heading>
            <Disclosure.Content>
              <Disclosure.Body className="mx-2 flex flex-col items-center gap-2 p-4 text-center">
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
                  Preview on Expo Go
                </Button>
              </Disclosure.Body>
            </Disclosure.Content>
          </Disclosure>
          <Separator className="my-2" />
          <Disclosure id="download">
            <Disclosure.Heading aria-label="Download HeroUI Native">
              <Button
                slot="trigger"
                variant={expandedKeys.has("download") ? "secondary" : "tertiary"}
                className={cn("w-full border-none", {
                  "bg-transparent": !expandedKeys.has("download"),
                })}
              >
                <div className="flex w-full items-center justify-start gap-2">
                  Download App
                </div>
                <Disclosure.Indicator className="text-muted" />
              </Button>
            </Disclosure.Heading>
            <Disclosure.Content>
              <Disclosure.Body className="mx-2 flex flex-col items-center gap-2 p-4 text-center">
                <p className="text-sm text-muted">
                  Download the HeroUI native app to explore our mobile components directly on your
                  device.
                </p>
                <img
                  alt="App Store QR Code"
                  className="aspect-square w-full max-w-54 object-cover"
                  src="https://heroui-assets.nyc3.cdn.digitaloceanspaces.com/images/qr-code-native.png"
                />
                <p className="text-sm text-muted">Available on iOS and Android devices.</p>
                <Button className="mt-4" variant="primary">
                  Download on App Store
                </Button>
              </Disclosure.Body>
            </Disclosure.Content>
          </Disclosure>
        </DisclosureGroup>
      </div>
    </div>
  );
}

export { Basic as Preview };
```
