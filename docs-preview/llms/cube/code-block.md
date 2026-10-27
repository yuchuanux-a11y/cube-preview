# CodeBlock

Cube component `CodeBlock` from `@bosagent/cube-ui/code-block`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/code-block` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/code-block` |

检索：CodeBlock、code-block。

## Import

```tsx
import { CodeBlock } from "@bosagent/cube-ui/code-block";
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
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `CodeBlock.Code`
- `CodeBlock.CopyButton`
- `CodeBlock.Header`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[CodeBlock](https://yuchuanux-a11y.github.io/cube-preview/#CodeBlock)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/code-block.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { CodeBlock } from '@components/code-block';

export function Default() {
  const code = `function greet(name: string) {
  return \`Hello, \${name}!\`;
}

console.log(greet("HeroUI"));`;

  return (
    <div className="w-[480px]">
      <CodeBlock>
        <CodeBlock.Header>
          <span className="text-xs text-muted uppercase">typescript</span>
          <CodeBlock.CopyButton code={code} />
        </CodeBlock.Header>
        <CodeBlock.Code code={code} language="typescript" />
      </CodeBlock>
    </div>
  );
}
```
