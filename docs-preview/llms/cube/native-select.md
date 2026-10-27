# NativeSelect

Cube component `NativeSelect` from `@bosagent/cube-ui/native-select`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/native-select` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/native-select` |

检索：NativeSelect、native-select。

## Import

```tsx
import { NativeSelect } from "@bosagent/cube-ui/native-select";
import { NativeSelect } from "@bosagent/cube-ui";
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
| `children` | `ReactNode` | Yes | `—` | — |
| `fullWidth` | `boolean` | No | `—` | Whether the select should take up the full width of its container. |
| `variant` | `"primary" \| "secondary"` | No | `"primary"` | The visual variant. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `NativeSelect.Indicator`
- `NativeSelect.OptGroup`
- `NativeSelect.Option`
- `NativeSelect.Trigger`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[NativeSelect](https://yuchuanux-a11y.github.io/cube-preview/#NativeSelect)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/native-select.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { NativeSelect } from '@components/native-select';

export function Default() {
  return (
    <div className="w-full max-w-[220px]">
      <NativeSelect className="w-full">
        <NativeSelect.Trigger>
          <NativeSelect.Option value="">Select status</NativeSelect.Option>
          <NativeSelect.Option value="todo">Todo</NativeSelect.Option>
          <NativeSelect.Option value="in-progress">
            In Progress
          </NativeSelect.Option>
          <NativeSelect.Option value="done">Done</NativeSelect.Option>
          <NativeSelect.Option value="cancelled">Cancelled</NativeSelect.Option>
          <NativeSelect.Indicator />
        </NativeSelect.Trigger>
      </NativeSelect>
    </div>
  );
}
```
