# Sheet

Cube component `Sheet` from `@bosagent/cube-ui/sheet`.

- 分层：Cube
- 包：`@bosagent/cube-ui/sheet`
- 状态：建设中

## Import

```tsx
import { Sheet } from "@bosagent/cube-ui/sheet";
import { Sheet } from "@bosagent/cube-ui";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `fadeFromIndex` | `number` | 是 | `—` | — |
| `snapPoints` | `(string \| number)[]` | 是 | `—` | — |
| `activeSnapPoint` | `string \| number` | 否 | `—` | — |
| `children` | `ReactNode` | 否 | `—` | — |
| `closeThreshold` | `number` | 否 | `—` | — |
| `container` | `HTMLElement` | 否 | `—` | — |
| `defaultOpen` | `boolean` | 否 | `—` | — |
| `disablePreventScroll` | `boolean` | 否 | `—` | — |
| `isDetached` | `boolean` | 否 | `—` | — |
| `isDismissable` | `boolean` | 否 | `—` | — |
| `isFixed` | `boolean` | 否 | `—` | — |
| `isHandleOnly` | `boolean` | 否 | `—` | — |
| `isModal` | `boolean` | 否 | `—` | — |
| `isNested` | `boolean` | 否 | `—` | — |
| `isOpen` | `boolean` | 否 | `—` | — |
| `noBodyStyles` | `boolean` | 否 | `—` | — |
| `placement` | `SheetPlacement` | 否 | `—` | — |
| `preventScrollRestoration` | `boolean` | 否 | `—` | — |
| `repositionInputs` | `boolean` | 否 | `—` | — |
| `scrollLockTimeout` | `number` | 否 | `—` | — |
| `setBackgroundColorOnScale` | `boolean` | 否 | `—` | — |
| `shouldAutoFocus` | `boolean` | 否 | `—` | — |
| `shouldScaleBackground` | `boolean` | 否 | `—` | — |
| `snapToSequentialPoint` | `boolean` | 否 | `—` | — |

<details className="not-prose my-6">
<summary className="cursor-pointer text-sm text-fd-muted-foreground">无障碍与事件</summary>

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `onActiveSnapPointChange` | `(snapPoint: number \| string \| null) => void` | 否 | `—` | — |
| `onAnimationEnd` | `(open: boolean) => void` | 否 | `—` | — |
| `onClose` | `() => void` | 否 | `—` | — |
| `onDrag` | `(event: React.PointerEvent<HTMLDivElement>, percentageDragged: number) => void` | 否 | `—` | — |
| `onOpenChange` | `(open: boolean) => void` | 否 | `—` | — |
| `onRelease` | `(event: React.PointerEvent<HTMLDivElement>, open: boolean) => void` | 否 | `—` | — |

</details>

## Parts

- `Sheet.Backdrop`
- `Sheet.Body`
- `Sheet.Close`
- `Sheet.CloseTrigger`
- `Sheet.Content`
- `Sheet.Dialog`
- `Sheet.Footer`
- `Sheet.Handle`
- `Sheet.Header`
- `Sheet.Heading`
- `Sheet.NestedRoot`
- `Sheet.Trigger`

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Sheet
