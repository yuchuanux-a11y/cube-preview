# Segment

Cube component `Segment` from `@bosagent/cube-ui/segment`.

- 分层：Cube
- 包：`@bosagent/cube-ui/segment`
- 状态：建设中

## Import

```tsx
import { Segment } from "@bosagent/cube-ui/segment";
import { Segment } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `className` | `string` | 否 | `'react-aria-ToggleButtonGroup'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultSelectedKey` | `Key` | 否 | `—` | — |
| `isDisabled` | `boolean` | 否 | `—` | Whether all items are disabled. |
| `selectedKey` | `Key` | 否 | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | 否 | `—` | — |
| `variant` | `"default" \| "ghost"` | 否 | `—` | — |
| `children` | `ChildrenOrFunction<ToggleButtonGroupRenderProps>` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `disallowEmptySelection` | `boolean` | 否 | `—` | Whether the collection allows empty selection. |
| `orientation` | `Orientation` | 否 | `'horizontal'` | The orientation of the the toggle button group. |
| `render` | `DOMRenderFunction<"div", ToggleButtonGroupRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ToggleButtonGroupRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onSelectionChange` | `(key: Key) => void` | 否 | `—` | — |

</details>

## Parts

- `Segment.Item`
- `Segment.Separator`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Segment
