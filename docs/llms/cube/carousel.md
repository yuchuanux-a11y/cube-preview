# Carousel

Cube component `Carousel` from `@bosagent/cube-ui/carousel`.

Cube component. Source: `packages/cube-ui/src/components/carousel`.

## Import

```tsx
import { Carousel } from "@bosagent/cube-ui/carousel";
```

## Figma

[Open Carousel in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=5375-80499)

## Preview

The docs page renders a live preview of the real component.

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

## Example source

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
