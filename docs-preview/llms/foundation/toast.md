# Toast

Display temporary notifications and messages to users with automatic dismissal and customizable placement

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：Toast、toast。

Native 目录说明：即时反馈操作结果。

## Import

```tsx
import { Toast } from "@heroui/react";
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
| `placement` | `"bottom" \| "top" \| "bottom start" \| "bottom end" \| "top start" \| "top end"` | No | `—` | — |
| `scaleFactor` | `number` | No | `0.05` | How much each toast behind the front one scales down. Inherited from the provider when omitted. |
| `variant` | `"default" \| "danger" \| "accent" \| "success" \| "warning"` | No | `—` | — |
| `toast` | `QueuedToast<T>` | Yes | `—` | The toast object. |
| `children` | `ChildrenOrFunction<ToastRenderProps<T>>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<ToastRenderProps<T>>` | No | `'react-aria-Toast'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `render` | `DOMRenderFunction<"div", ToastRenderProps<T>>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `style` | `StyleOrFunction<ToastRenderProps<T>>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `Toast.ActionButton`
- `Toast.CloseButton`
- `Toast.Content`
- `Toast.Description`
- `Toast.Indicator`
- `Toast.Provider`
- `Toast.Title`
- `Toast.toast`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open Toast in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-72573)

## 画廊

[Toast](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Toast)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/toast.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Persons} from "@gravity-ui/icons";
import {Button, toast} from "@heroui/react";

export function Default() {
  return (
    <div className="flex h-full max-w-xl flex-col items-center justify-center">
      <Button
        size="sm"
        variant="secondary"
        onPress={() => {
          const id = toast("You have been invited to join a team", {
            actionProps: {
              children: "Dismiss",
              onPress: () => toast.close(id),
              variant: "tertiary",
            },
            description: "Bob sent you an invitation to join HeroUI team",
            indicator: <Persons />,
            variant: "default",
          });
        }}
      >
        Show toast
      </Button>
    </div>
  );
}

export { Default as Preview };
```
