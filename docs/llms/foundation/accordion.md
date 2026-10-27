# Accordion

A collapsible content panel for organizing information in a compact space

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { Accordion } from "@heroui/react";
```

## Figma

[Open Accordion in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-79876)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `hideSeparator` | `boolean` | No | `—` | — |
| `variant` | `"default" \| "surface"` | No | `—` | — |
| `allowsMultipleExpanded` | `boolean` | No | `—` | Whether multiple items can be expanded at the same time. |
| `children` | `ChildrenOrFunction<DisclosureGroupRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<DisclosureGroupRenderProps>` | No | `'react-aria-DisclosureGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultExpandedKeys` | `Iterable<Key>` | No | `—` | The initial expanded keys in the group (uncontrolled). |
| `expandedKeys` | `Iterable<Key>` | No | `—` | The currently expanded keys in the group (controlled). |
| `isDisabled` | `boolean` | No | `—` | Whether all items are disabled. |
| `onExpandedChange` | `(keys: Set<Key>) => any` | No | `—` | Handler that is called when items are expanded or collapsed. |
| `render` | `DOMRenderFunction<"div", DisclosureGroupRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `style` | `StyleOrFunction<DisclosureGroupRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `Accordion.Body`
- `Accordion.Heading`
- `Accordion.Indicator`
- `Accordion.Item`
- `Accordion.Panel`
- `Accordion.Trigger`

## Example source

```tsx
'use client';

import {
  ArrowsRotateLeft,
  Box,
  ChevronDown,
  CreditCard,
  PlanetEarth,
  Receipt,
  ShoppingBag,
} from "@gravity-ui/icons";
import {Accordion} from "@heroui/react";

const items = [
  {
    content:
      "Browse our products, add items to your cart, and proceed to checkout. You'll need to provide shipping and payment information to complete your purchase.",
    icon: <ShoppingBag />,
    title: "How do I place an order?",
  },
  {
    content:
      "Yes, you can modify or cancel your order before it's shipped. Once your order is processed, you can't make changes.",
    icon: <Receipt />,
    title: "Can I modify or cancel my order?",
  },
  {
    content: "We accept all major credit cards, including Visa, Mastercard, and American Express.",
    icon: <CreditCard />,
    title: "What payment methods do you accept?",
  },
  {
    content:
      "Shipping costs vary based on your location and the size of your order. We offer free shipping for orders over $50.",
    icon: <Box />,
    title: "How much does shipping cost?",
  },
  {
    content:
      "Yes, we ship to most countries. Please check our shipping rates and policies for more information.",
    icon: <PlanetEarth />,
    title: "Do you ship internationally?",
  },
  {
    content:
      "If you're not satisfied with your purchase, you can request a refund within 30 days of purchase. Please contact our customer support team for assistance.",
    icon: <ArrowsRotateLeft />,
    title: "How do I request a refund?",
  },
];

export function Basic() {
  return (
    <Accordion className="w-full max-w-md">
      {items.map((item, index) => (
        <Accordion.Item key={index}>
          <Accordion.Heading>
            <Accordion.Trigger>
              {item.icon ? (
                <span className="me-3 size-4 shrink-0 text-muted">{item.icon}</span>
              ) : null}
              {item.title}
              <Accordion.Indicator>
                <ChevronDown />
              </Accordion.Indicator>
            </Accordion.Trigger>
          </Accordion.Heading>
          <Accordion.Panel>
            <Accordion.Body>{item.content}</Accordion.Body>
          </Accordion.Panel>
        </Accordion.Item>
      ))}
    </Accordion>
  );
}

export { Basic as Preview };
```
