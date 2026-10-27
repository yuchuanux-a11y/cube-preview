# InputOTP

A one-time password input component for verification codes and secure authentication

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { InputOTP } from "@heroui/react";
```

## Figma

[Open InputOTP in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-69951)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | Yes | `—` | — |
| `inputClassName` | `string` | No | `—` | — |
| `isDisabled` | `boolean` | No | `—` | — |
| `isInvalid` | `boolean` | No | `—` | — |
| `validationDetails` | `ValidityState` | No | `—` | — |
| `validationErrors` | `string[]` | No | `—` | — |
| `variant` | `"primary" \| "secondary"` | No | `—` | — |
| `maxLength` | `number` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `nonce` | `string` | No | `—` | — |
| `noScriptCSSFallback` | `string` | No | `—` | — |
| `onChange` | `(newValue: string) => unknown` | No | `—` | — |
| `onComplete` | `(...args: any[]) => unknown` | No | `—` | — |
| `pasteTransformer` | `(pasted: string) => string` | No | `—` | — |
| `pushPasswordManagerStrategy` | `"none" \| "increase-width"` | No | `—` | — |
| `slot` | `string` | No | `—` | — |
| `textAlign` | `"center" \| "left" \| "right"` | No | `—` | — |
| `value` | `string` | No | `—` | — |

## Parts

- `InputOTP.Group`
- `InputOTP.Separator`
- `InputOTP.Slot`

## Example source

```tsx
'use client';

import {InputOTP, Label, Link} from "@heroui/react";

export function Basic() {
  return (
    <div className="flex w-[280px] flex-col gap-2">
      <div className="flex flex-col gap-1">
        <Label>Verify account</Label>
        <p className="text-sm text-muted">We&apos;ve sent a code to a****@gmail.com</p>
      </div>
      <InputOTP maxLength={6}>
        <InputOTP.Group>
          <InputOTP.Slot index={0} />
          <InputOTP.Slot index={1} />
          <InputOTP.Slot index={2} />
        </InputOTP.Group>
        <InputOTP.Separator />
        <InputOTP.Group>
          <InputOTP.Slot index={3} />
          <InputOTP.Slot index={4} />
          <InputOTP.Slot index={5} />
        </InputOTP.Group>
      </InputOTP>
      <div className="flex items-center gap-[5px] px-1 pt-1">
        <p className="text-sm text-muted">Didn&apos;t receive a code?</p>
        <Link className="text-foreground underline" href="#">
          Resend
        </Link>
      </div>
    </div>
  );
}

export { Basic as Preview };
```
