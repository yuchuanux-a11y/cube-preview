# Sheet

Cube component `Sheet` from `@bosagent/cube-ui/sheet`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/sheet` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/sheet` |

检索：Sheet、sheet。

## Import

```tsx
import { Sheet } from "@bosagent/cube-ui/sheet";
import { Sheet } from "@bosagent/cube-ui";
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
| `fadeFromIndex` | `number` | Yes | `—` | — |
| `snapPoints` | `(string \| number)[]` | Yes | `—` | — |
| `activeSnapPoint` | `string \| number` | No | `—` | — |
| `children` | `ReactNode` | No | `—` | — |
| `closeThreshold` | `number` | No | `—` | — |
| `container` | `HTMLElement` | No | `—` | — |
| `defaultOpen` | `boolean` | No | `—` | — |
| `disablePreventScroll` | `boolean` | No | `—` | — |
| `isDetached` | `boolean` | No | `—` | — |
| `isDismissable` | `boolean` | No | `—` | — |
| `isFixed` | `boolean` | No | `—` | — |
| `isHandleOnly` | `boolean` | No | `—` | — |
| `isModal` | `boolean` | No | `—` | — |
| `isNested` | `boolean` | No | `—` | — |
| `isOpen` | `boolean` | No | `—` | — |
| `noBodyStyles` | `boolean` | No | `—` | — |
| `onActiveSnapPointChange` | `(snapPoint: number \| string \| null) => void` | No | `—` | — |
| `onAnimationEnd` | `(open: boolean) => void` | No | `—` | — |
| `onClose` | `() => void` | No | `—` | — |
| `onDrag` | `(event: React.PointerEvent<HTMLDivElement>, percentageDragged: number) => void` | No | `—` | — |
| `onOpenChange` | `(open: boolean) => void` | No | `—` | — |
| `onRelease` | `(event: React.PointerEvent<HTMLDivElement>, open: boolean) => void` | No | `—` | — |
| `placement` | `SheetPlacement` | No | `—` | — |
| `preventScrollRestoration` | `boolean` | No | `—` | — |
| `repositionInputs` | `boolean` | No | `—` | — |
| `scrollLockTimeout` | `number` | No | `—` | — |
| `setBackgroundColorOnScale` | `boolean` | No | `—` | — |
| `shouldAutoFocus` | `boolean` | No | `—` | — |
| `shouldScaleBackground` | `boolean` | No | `—` | — |
| `snapToSequentialPoint` | `boolean` | No | `—` | — |

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

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[Sheet](https://yuchuanux-a11y.github.io/cube-preview/#Sheet)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/sheet.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { Sheet } from '@components/sheet';
import { Button } from '@heroui/react';

export function Default() {
  return (
    <Sheet>
      <Sheet.Trigger>
        <Button variant="secondary">Open Sheet</Button>
      </Sheet.Trigger>
      <Sheet.Backdrop>
        <Sheet.Content className="mx-auto max-h-[95vh] max-w-[420px]">
          <Sheet.Dialog>
            <Sheet.Handle />
            <Sheet.CloseTrigger />
            <Sheet.Header>
              <Sheet.Heading>Sheet Title</Sheet.Heading>
            </Sheet.Header>
            <Sheet.Body>
              <p className="text-sm text-muted">
                This is a bottom sheet built with smooth drag-to-dismiss
                animations. Try dragging it down to close, or use the close
                button.
              </p>
            </Sheet.Body>
            <Sheet.Footer>
              <Sheet.Close>
                <Button variant="secondary">Cancel</Button>
              </Sheet.Close>
              <Sheet.Close>
                <Button>Confirm</Button>
              </Sheet.Close>
            </Sheet.Footer>
          </Sheet.Dialog>
        </Sheet.Content>
      </Sheet.Backdrop>
    </Sheet>
  );
}
```
