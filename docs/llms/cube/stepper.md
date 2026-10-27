# Stepper

Cube component `Stepper` from `@bosagent/cube-ui/stepper`.

Cube component. Source: `packages/cube-ui/src/components/stepper`.

## Import

```tsx
import { Stepper } from "@bosagent/cube-ui/stepper";
import { Stepper } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
