# ChatTool

Cube component `ChatTool` from `@bosagent/cube-ui/chat-tool`.

- 分层：Cube
- 包：`@bosagent/cube-ui/chat-tool`
- 状态：建设中

## Import

```tsx
import { ChatTool } from "@bosagent/cube-ui/chat-tool";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `state` | `ToolPartState` | 是 | `—` | — |
| `active` | `boolean` | 否 | `—` | Controls shimmer styling for running tools. Defaults to running when the state is in progress. |
| `approveLabel` | `ReactNode` | 否 | `—` | — |
| `argsText` | `string` | 否 | `—` | — |
| `children` | `ReactNode` | 否 | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `errorText` | `string` | 否 | `—` | — |
| `input` | `unknown` | 否 | `—` | — |
| `isExpandable` | `boolean` | 否 | `—` | Whether the tool row can expand to reveal body content. Defaults to true for custom children. |
| `output` | `unknown` | 否 | `—` | — |
| `rejectLabel` | `ReactNode` | 否 | `—` | — |
| `toolCallId` | `string` | 否 | `—` | — |
| `toolName` | `string` | 否 | `—` | — |
| `triggerPrefix` | `ReactNode` | 否 | `—` | Preset: optional label before the tool name in the default trigger. |
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
| `onApprove` | `() => void` | 否 | `—` | Preset: called when the user approves a tool that requires action. |
| `onReject` | `() => void` | 否 | `—` | Preset: called when the user rejects a tool that requires action. |
| `onExpandedChange` | `(isExpanded: boolean) => void` | 否 | `—` | Handler that is called when the disclosure's expanded state changes. |

</details>

## Parts

- `ChatTool.Approval`
- `ChatTool.ApprovalActions`
- `ChatTool.Approve`
- `ChatTool.Args`
- `ChatTool.Content`
- `ChatTool.Error`
- `ChatTool.Meta`
- `ChatTool.Reject`
- `ChatTool.Result`
- `ChatTool.StatusIcon`
- `ChatTool.Trigger`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#ChatTool
