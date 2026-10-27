# ActionBar

Cube component `ActionBar` from `@bosagent/cube-ui/action-bar`.

- 分层：Cube
- 包：`@bosagent/cube-ui/action-bar`
- 状态：建设中

## Import

```tsx
import { ActionBar } from "@bosagent/cube-ui/action-bar";
import { ActionBar } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `isOpen` | `boolean` | 是 | `—` | Controls visibility with animated enter/exit. |
| `isAttached` | `boolean` | 否 | `—` | — |
| `className` | `ClassNameOrFunction<ToolbarRenderProps>` | 否 | `'react-aria-Toolbar'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `orientation` | `Orientation` | 否 | `'horizontal'` | The orientation of the entire toolbar. |
| `render` | `DOMRenderFunction<"div", ToolbarRenderProps>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | 否 | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<ToolbarRenderProps>` | 否 | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `ActionBar.Content`
- `ActionBar.Prefix`
- `ActionBar.Suffix`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#ActionBar
