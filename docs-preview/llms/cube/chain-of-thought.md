# ChainOfThought

Cube component `ChainOfThought` from `@bosagent/cube-ui/chain-of-thought`.

- 分层：Cube
- 包：`@bosagent/cube-ui/chain-of-thought`
- 状态：建设中

## Import

```tsx
import { ChainOfThought } from "@bosagent/cube-ui/chain-of-thought";
import { ChainOfThought } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `isStreaming` | `boolean` | 否 | `—` | Show shimmer styling on the trigger while reasoning is in progress. |
| `className` | `ClassNameOrFunction<DisclosureRenderProps>` | 否 | `'react-aria-Disclosure'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultExpanded` | `boolean` | 否 | `—` | Whether the disclosure is expanded by default (uncontrolled). |
| `id` | `Key` | 否 | `—` | An id for the disclosure when used within a DisclosureGroup, matching the id used in `expandedKeys`. |
| `isDisabled` | `boolean` | 否 | `—` | Whether the disclosure is disabled. |
| `isExpanded` | `boolean` | 否 | `—` | Whether the disclosure is expanded (controlled). |
| `render` | `DOMRenderFunction<"div", DisclosureRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<DisclosureRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onExpandedChange` | `(isExpanded: boolean) => void` | 否 | `—` | Handler that is called when the disclosure's expanded state changes. |

</details>

## Parts

- `ChainOfThought.Content`
- `ChainOfThought.Step`
- `ChainOfThought.Steps`
- `ChainOfThought.Trigger`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#ChainOfThought
