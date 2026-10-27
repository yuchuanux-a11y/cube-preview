# Stepper

Cube component `Stepper` from `@bosagent/cube-ui/stepper`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/stepper` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/stepper` |

检索：Stepper、stepper。

## Import

```tsx
import { Stepper } from "@bosagent/cube-ui/stepper";
import { Stepper } from "@bosagent/cube-ui";
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
| `children` | `React.ReactNode` | Yes | `—` | — |
| `currentStep` | `number` | No | `—` | — |
| `defaultStep` | `number` | No | `—` | — |
| `onStepChange` | `(step: number) => void` | No | `—` | — |
| `orientation` | `"horizontal" \| "vertical"` | No | `—` | — |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `Stepper.Content`
- `Stepper.Description`
- `Stepper.Icon`
- `Stepper.Indicator`
- `Stepper.Separator`
- `Stepper.Step`
- `Stepper.Title`
- `Stepper.useStep`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[Stepper](https://yuchuanux-a11y.github.io/cube-preview/#Stepper)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/stepper.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { useState } from 'react';
import { Stepper } from '@components/stepper';

const steps = [
  { title: 'Cart' },
  { title: 'Shipping' },
  { title: 'Payment' },
  { title: 'Confirmation' },
];

export function Default() {
  const [step, setStep] = useState(1);

  return (
    <div className="w-[500px]">
      <Stepper currentStep={step} onStepChange={setStep}>
        {steps.map((s) => (
          <Stepper.Step key={s.title}>
            <Stepper.Indicator />
            <Stepper.Content>
              <Stepper.Title>{s.title}</Stepper.Title>
            </Stepper.Content>
            <Stepper.Separator />
          </Stepper.Step>
        ))}
      </Stepper>
    </div>
  );
}
```
