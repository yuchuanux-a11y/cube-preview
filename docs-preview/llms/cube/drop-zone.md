# DropZone

Cube component `DropZone` from `@bosagent/cube-ui/drop-zone`.

- 分层：Cube
- 包：`@bosagent/cube-ui/drop-zone`
- 状态：建设中

## Import

```tsx
import { DropZone } from "@bosagent/cube-ui/drop-zone";
import { DropZone } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `ReactNode` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | 否 | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | 否 | `—` | — |

## Parts

- `DropZone.Area`
- `DropZone.Description`
- `DropZone.FileFormatIcon`
- `DropZone.FileInfo`
- `DropZone.FileItem`
- `DropZone.FileList`
- `DropZone.FileMeta`
- `DropZone.FileName`
- `DropZone.FileProgress`
- `DropZone.FileProgressFill`
- `DropZone.FileProgressTrack`
- `DropZone.FileRemoveTrigger`
- `DropZone.FileRetryTrigger`
- `DropZone.Icon`
- `DropZone.Input`
- `DropZone.Label`
- `DropZone.Trigger`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#DropZone
