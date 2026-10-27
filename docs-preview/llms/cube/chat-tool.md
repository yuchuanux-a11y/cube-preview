# ChatTool

Cube component `ChatTool` from `@bosagent/cube-ui/chat-tool`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/chat-tool` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/chat-tool` |

检索：ChatTool、chat-tool。

## Import

```tsx
import { ChatTool } from "@bosagent/cube-ui/chat-tool";
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
| `state` | `ToolPartState` | Yes | `—` | — |
| `active` | `boolean` | No | `—` | Controls shimmer styling for running tools. Defaults to running when the state is in progress. |
| `approveLabel` | `ReactNode` | No | `—` | — |
| `argsText` | `string` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `errorText` | `string` | No | `—` | — |
| `input` | `unknown` | No | `—` | — |
| `isExpandable` | `boolean` | No | `—` | Whether the tool row can expand to reveal body content. Defaults to true for custom children. |
| `onApprove` | `() => void` | No | `—` | Preset: called when the user approves a tool that requires action. |
| `onReject` | `() => void` | No | `—` | Preset: called when the user rejects a tool that requires action. |
| `output` | `unknown` | No | `—` | — |
| `rejectLabel` | `ReactNode` | No | `—` | — |
| `toolCallId` | `string` | No | `—` | — |
| `toolName` | `string` | No | `—` | — |
| `triggerPrefix` | `ReactNode` | No | `—` | Preset: optional label before the tool name in the default trigger. |
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

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ChatTool](https://yuchuanux-a11y.github.io/cube-preview/#ChatTool)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/chat-tool.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import type { ReactNode } from 'react';
import { ChatMessage } from '@components/chat-message';
import type { ToolPartState } from '@components/chat-tool';
import { ChatTool, ChatToolGroup } from '@components/chat-tool';

function AssistantMessage({ children }: { children: ReactNode }) {
  return (
    <ChatMessage.Assistant>
      <ChatMessage.Avatar show alt="Assistant" fallback="AI" />
      <ChatMessage.Body>{children}</ChatMessage.Body>
    </ChatMessage.Assistant>
  );
}

export function Default() {
  return (
    <AssistantMessage>
      <ChatMessage.Content>
        Completed tool call with JSON args and result.
      </ChatMessage.Content>
      <ChatTool
        argsText='{"city":"Paris"}'
        defaultExpanded={false}
        output={{ summary: '18°C, partly cloudy' }}
        state="output-available"
        toolName="getWeather"
        triggerPrefix="Used tool: "
      />
    </AssistantMessage>
  );
}

export function Streaming() {
  return (
    <AssistantMessage>
      <ChatTool
        defaultExpanded
        argsText='{"query":"Cube UI'
        state="input-streaming"
        toolName="searchDocs"
        triggerPrefix="Running tool: "
      />
    </AssistantMessage>
  );
}

export function ErrorState() {
  return (
    <AssistantMessage>
      <ChatTool
        defaultExpanded
        argsText='{"url":"https://example.com"}'
        errorText="Request timed out after 30s"
        state="output-error"
        toolName="fetchPage"
        triggerPrefix="Failed tool: "
      />
    </AssistantMessage>
  );
}

export function Approval() {
  return (
    <AssistantMessage>
      <ChatTool
        defaultExpanded
        approveLabel="Approve"
        argsText='{"to":"team@acme.com","subject":"Launch update"}'
        rejectLabel="Reject"
        state="requires-action"
        toolName="sendEmail"
        triggerPrefix="Approval needed: "
        onApprove={() => undefined}
        onReject={() => undefined}
      />
    </AssistantMessage>
  );
}

export function Composable() {
  return (
    <AssistantMessage>
      <ChatTool
        defaultExpanded={false}
        state="output-available"
        toolName="getWeather"
      >
        <ChatTool.Trigger>
          <ChatTool.StatusIcon />
          Used tool: <strong>getWeather</strong>
        </ChatTool.Trigger>
        <ChatTool.Content>
          <ChatTool.Args input={{ city: 'Paris' }} label="Parameters" />
          <ChatTool.Result
            label="Result"
            value={{ summary: '18°C, partly cloudy' }}
          />
        </ChatTool.Content>
      </ChatTool>
    </AssistantMessage>
  );
}

export function Grouped() {
  const tools: Array<{ state: ToolPartState; toolName: string }> = [
    { state: 'output-available', toolName: 'searchDocs' },
    { state: 'output-available', toolName: 'fetchPage' },
  ];

  return (
    <AssistantMessage>
      <ChatToolGroup defaultExpanded={false}>
        <ChatToolGroup.Trigger>2 tool calls</ChatToolGroup.Trigger>
        <ChatToolGroup.Content>
          {tools.map((tool) => (
            <ChatTool
              key={tool.toolName}
              defaultExpanded={false}
              state={tool.state}
              toolName={tool.toolName}
              triggerPrefix="Used tool: "
            />
          ))}
        </ChatToolGroup.Content>
      </ChatToolGroup>
    </AssistantMessage>
  );
}
```
