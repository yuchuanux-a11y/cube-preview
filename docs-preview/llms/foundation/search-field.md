# SearchField

Search input field with clear button and search icon

| 项目 | 内容 |
| --- | --- |
| 包 | `@heroui/react` |
| 分层 | Foundation |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |

检索：SearchField、search-field。

Native 目录说明：输入搜索关键词并清除查询。

## Import

```tsx
import { SearchField } from "@heroui/react";
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
| `fullWidth` | `boolean` | No | `—` | — |
| `variant` | `"primary" \| "secondary"` | No | `—` | — |
| `aria-activedescendant` | `string` | No | `—` | Identifies the currently active element when DOM focus is on a composite widget, textbox, group, or application. |
| `aria-autocomplete` | `"none" \| "list" \| "both" \| "inline"` | No | `—` | Indicates whether inputting text could trigger display of one or more predictions of the user's intended value for an input and specifies how predictions would be presented if they are made. |
| `aria-controls` | `string` | No | `—` | Identifies the element (or elements) whose contents or presence are controlled by the current element. |
| `aria-haspopup` | `boolean \| "true" \| "false" \| "dialog" \| "menu" \| "grid" \| "listbox" \| "tree"` | No | `—` | Indicates the availability and type of interactive popup element, such as menu or dialog, that can be triggered by an element. |
| `autoFocus` | `boolean` | No | `—` | Whether the element should receive focus on render. |
| `children` | `ChildrenOrFunction<SearchFieldRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<SearchFieldRenderProps>` | No | `'react-aria-SearchField'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `defaultValue` | `string` | No | `—` | The default value (uncontrolled). |
| `enterKeyHint` | `"search" \| "enter" \| "done" \| "go" \| "next" \| "previous" \| "send"` | No | `—` | An enumerated attribute that defines what action label or icon to preset for the enter key on virtual keyboards. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/enterkeyhint). |
| `isDisabled` | `boolean` | No | `—` | Whether the input is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the input value is invalid. |
| `isReadOnly` | `boolean` | No | `—` | Whether the input can be selected but not changed by the user. |
| `isRequired` | `boolean` | No | `—` | Whether user input is required on the input before form submission. |
| `onBlur` | `(e: FocusEvent<HTMLInputElement, Element>) => void` | No | `—` | Handler that is called when the element loses focus. |
| `onChange` | `(value: string) => void` | No | `—` | Handler that is called when the value changes. |
| `onClear` | `() => void` | No | `—` | Handler that is called when the clear button is pressed. |
| `onFocus` | `(e: FocusEvent<HTMLInputElement, Element>) => void` | No | `—` | Handler that is called when the element receives focus. |
| `onFocusChange` | `(isFocused: boolean) => void` | No | `—` | Handler that is called when the element's focus status changes. |
| `onKeyDown` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is pressed. |
| `onKeyUp` | `(e: KeyboardEvent) => void` | No | `—` | Handler that is called when a key is released. |
| `onSubmit` | `(value: string) => void` | No | `—` | Handler that is called when the SearchField is submitted. |
| `render` | `DOMRenderFunction<"div", SearchFieldRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<SearchFieldRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |
| `type` | `"search" \| "text" \| (string & {}) \| "tel" \| "url" \| "email" \| "password"` | No | `'search'` | The type of input to render. See [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdeftype). |
| `validate` | `(value: string) => ValidationError \| true \| null \| undefined` | No | `—` | A function that returns an error message if a given value is invalid. Validation errors are displayed to the user when the form is submitted if `validationBehavior="native"`. For realtime validation, use the `isInvalid` prop instead. |
| `validationBehavior` | `"native" \| "aria"` | No | `'native'` | Whether to use native HTML form validation to prevent form submission when the value is missing or invalid, or mark the field as required or invalid via ARIA. |
| `value` | `string` | No | `—` | The current value (controlled). |

## Parts

- `SearchField.ClearButton`
- `SearchField.Group`
- `SearchField.Input`
- `SearchField.SearchIcon`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open SearchField in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=17293-34733)

## 画廊

[SearchField](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/SearchField)

公开画廊的 Native 目录有同名入口。Web Demo 目录没有这个 Foundation 组件的独立页面。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/foundation/search-field.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import {Label, SearchField} from "@heroui/react";

export function Basic() {
  return (
    <SearchField name="search">
      <Label>Search</Label>
      <SearchField.Group>
        <SearchField.SearchIcon />
        <SearchField.Input className="w-[280px]" placeholder="Search..." />
        <SearchField.ClearButton />
      </SearchField.Group>
    </SearchField>
  );
}

export { Basic as Preview };
```
