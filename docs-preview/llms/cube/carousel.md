# Carousel

Cube component `Carousel` from `@bosagent/cube-ui/carousel`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/carousel` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/carousel` |

检索：Carousel、carousel。

## Import

```tsx
import { Carousel } from "@bosagent/cube-ui/carousel";
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
| `opts` | `Partial<OptionsType>` | No | `—` | Embla Carousel options. |
| `plugins` | `CreatePluginType<LoosePluginType, {}>[]` | No | `—` | Embla Carousel plugins. |
| `setApi` | `(api: EmblaCarouselType) => void` | No | `—` | Callback to receive the Embla API instance. |
| `type` | `"modal" \| "in-place" \| "miniatures"` | No | `"in-place"` | Carousel type. |
| `children` | `ReactNode` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `Carousel.Content`
- `Carousel.Dots`
- `Carousel.Item`
- `Carousel.Next`
- `Carousel.Previous`
- `Carousel.Thumbnail`
- `Carousel.Thumbnails`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## Figma

[Open Carousel in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-80499)

## 画廊

[Carousel](https://yuchuanux-a11y.github.io/cube-preview/#Carousel)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/carousel.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { Carousel } from '@components/carousel';

const images = [
  {
    alt: 'Sneakers front view',
    src: 'https://nextuipro.nyc3.cdn.digitaloceanspaces.com/components-images/shoes/product-view/1.jpeg',
  },
  {
    alt: 'Sneakers side view',
    src: 'https://nextuipro.nyc3.cdn.digitaloceanspaces.com/components-images/shoes/product-view/2.jpeg',
  },
  {
    alt: 'Sneakers back view',
    src: 'https://nextuipro.nyc3.cdn.digitaloceanspaces.com/components-images/shoes/product-view/3.jpeg',
  },
  {
    alt: 'Sneakers top view',
    src: 'https://nextuipro.nyc3.cdn.digitaloceanspaces.com/components-images/shoes/product-view/4.jpeg',
  },
  {
    alt: 'Sneakers detail view',
    src: 'https://nextuipro.nyc3.cdn.digitaloceanspaces.com/components-images/shoes/product-view/5.jpeg',
  },
  {
    alt: 'Sneakers sole view',
    src: 'https://nextuipro.nyc3.cdn.digitaloceanspaces.com/components-images/shoes/product-view/6.jpeg',
  },
];

export function Default() {
  return (
    <div className="w-full max-w-sm">
      <Carousel opts={{ loop: true }}>
        <Carousel.Content>
          {images.map((image, i) => (
            <Carousel.Item key={i}>
              <div className="overflow-hidden rounded-3xl">
                <img
                  alt={image.alt}
                  className="aspect-square w-full object-cover select-none"
                  draggable={false}
                  src={image.src}
                />
              </div>
            </Carousel.Item>
          ))}
        </Carousel.Content>
        <Carousel.Previous />
        <Carousel.Next />
        <Carousel.Dots />
        <Carousel.Thumbnails>
          {images.map((image, i) => (
            <Carousel.Thumbnail
              key={i}
              alt={image.alt}
              index={i}
              src={image.src}
            />
          ))}
        </Carousel.Thumbnails>
      </Carousel>
    </div>
  );
}
```
