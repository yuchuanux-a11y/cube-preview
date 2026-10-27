# Carousel

Cube component `Carousel` from `@bosagent/cube-ui/carousel`.

- 分层：Cube
- 包：`@bosagent/cube-ui/carousel`
- 状态：建设中

## Import

```tsx
import { Carousel } from "@bosagent/cube-ui/carousel";
```

## Props

## 属性

| 属性 | 类型 | 必填 | 默认 | 说明 |
| --- | --- | --- | --- | --- |
| `opts` | `Partial<OptionsType>` | 否 | `—` | Embla Carousel options. |
| `plugins` | `CreatePluginType<LoosePluginType, {}>[]` | 否 | `—` | Embla Carousel plugins. |
| `setApi` | `(api: EmblaCarouselType) => void` | 否 | `—` | Callback to receive the Embla API instance. |
| `type` | `"modal" \| "in-place" \| "miniatures"` | 否 | `"in-place"` | Carousel type. |
| `children` | `ReactNode` | 否 | `—` | — |
| `className` | `string` | 否 | `—` | — |
| `slot` | `string` | 否 | `—` | — |

## Parts

- `Carousel.Content`
- `Carousel.Dots`
- `Carousel.Item`
- `Carousel.Next`
- `Carousel.Previous`
- `Carousel.Thumbnail`
- `Carousel.Thumbnails`

## Figma

https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-80499

## 画廊

https://yuchuanux-a11y.github.io/cube-preview/#Carousel
