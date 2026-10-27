# InputOTP

A one-time password input component for verification codes and secure authentication

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：InputOTP、input-otp。

Native 目录说明：分段输入一次性验证码。

## Import

```tsx
import { InputOTP } from "@heroui/react";
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

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open InputOTP in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-69951)

## 画廊

[InputOTP](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/InputOTP)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/input-otp.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

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
