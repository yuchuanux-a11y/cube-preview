# CodeBlock

Cube component `CodeBlock` from `@bosagent/cube-ui/code-block`.

Cube component. Source: `packages/cube-ui/src/components/code-block`.

## Import

```tsx
import { CodeBlock } from "@bosagent/cube-ui/code-block";
```

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
