# InputOTP

A one-time password input component for verification codes and secure authentication

- 分层：Foundation
- 包：`@heroui/react`
- 状态：建设中

## Import

```tsx
import { InputOTP } from "@heroui/react";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | 是 | `—` | — |
| `inputClassName` | `string` | 否 | `—` | — |
| `isDisabled` | `boolean` | 否 | `—` | — |
| `isInvalid` | `boolean` | 否 | `—` | — |
| `validationDetails` | `ValidityState` | 否 | `—` | — |
| `validationErrors` | `string[]` | 否 | `—` | — |
| `variant` | `"primary" \| "secondary"` | 否 | `—` | — |
| `maxLength` | `number` | 是 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `nonce` | `string` | 否 | `—` | — |
| `noScriptCSSFallback` | `string` | 否 | `—` | — |
| `pasteTransformer` | `(pasted: string) => string` | 否 | `—` | — |
| `pushPasswordManagerStrategy` | `"none" \| "increase-width"` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |
| `textAlign` | `"center" \| "left" \| "right"` | 否 | `—` | — |
| `value` | `string` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onChange` | `(newValue: string) => unknown` | 否 | `—` | — |
| `onComplete` | `(...args: any[]) => unknown` | 否 | `—` | — |

</details>

## Parts

- `InputOTP.Group`
- `InputOTP.Separator`
- `InputOTP.Slot`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-69951

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Mobile/InputOTP
