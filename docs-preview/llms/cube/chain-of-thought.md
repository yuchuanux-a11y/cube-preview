# ChainOfThought

Cube component `ChainOfThought` from `@bosagent/cube-ui/chain-of-thought`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/chain-of-thought` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/chain-of-thought` |

检索：ChainOfThought、chain-of-thought。

## Import

```tsx
import { ChainOfThought } from "@bosagent/cube-ui/chain-of-thought";
import { ChainOfThought } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## 适用

建设中。设计 registry 没有这条用法。

## 不适用

建设中。

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | Yes | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `isStreaming` | `boolean` | No | `—` | Show shimmer styling on the trigger while reasoning is in progress. |
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

- `ChainOfThought.Content`
- `ChainOfThought.Step`
- `ChainOfThought.Steps`
- `ChainOfThought.Trigger`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ChainOfThought](https://yuchuanux-a11y.github.io/cube-preview/#ChainOfThought)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/chain-of-thought.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { ChainOfThought } from '@components/chain-of-thought';

export function Default() {
  return (
    <div className="w-full max-w-[640px]">
      <ChainOfThought defaultExpanded={false}>
        <ChainOfThought.Trigger>Thought for 4 seconds</ChainOfThought.Trigger>
        <ChainOfThought.Content>
          <ChainOfThought.Steps>
            <ChainOfThought.Step label="Search">
              Looked up Cube UI chat template patterns for message layout and
              composer spacing.
            </ChainOfThought.Step>
            <ChainOfThought.Step label="Plan">
              Mapped the template structure to SDK-agnostic compound components.
            </ChainOfThought.Step>
          </ChainOfThought.Steps>
        </ChainOfThought.Content>
      </ChainOfThought>
    </div>
  );
}

export function Streaming() {
  return (
    <div className="w-full max-w-[640px]">
      <ChainOfThought isExpanded isStreaming>
        <ChainOfThought.Trigger>Thinking...</ChainOfThought.Trigger>
        <ChainOfThought.Content>
          <ChainOfThought.Steps>
            <ChainOfThought.Step label="Analyze">
              Breaking the request into presentation-only Pro components.
            </ChainOfThought.Step>
          </ChainOfThought.Steps>
        </ChainOfThought.Content>
      </ChainOfThought>
    </div>
  );
}
```
