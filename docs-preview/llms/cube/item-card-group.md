# ItemCardGroup

Cube component `ItemCardGroup` from `@bosagent/cube-ui/item-card-group`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/item-card-group` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/item-card-group` |

检索：ItemCardGroup、item-card-group。

## Import

```tsx
import { ItemCardGroup } from "@bosagent/cube-ui/item-card-group";
import { ItemCardGroup } from "@bosagent/cube-ui";
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
| `children` | `ReactNode` | Yes | `—` | — |
| `columns` | `2 \| 3` | No | `2` | Number of grid columns when layout is "grid". |
| `layout` | `"grid" \| "list"` | No | `"list"` | Layout mode. |
| `variant` | `"outline" \| "default" \| "secondary" \| "tertiary" \| "transparent"` | No | `"default"` | Visual variant. |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `ItemCardGroup.Description`
- `ItemCardGroup.Header`
- `ItemCardGroup.Title`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[ItemCardGroup](https://yuchuanux-a11y.github.io/cube-preview/#ItemCardGroup)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/item-card-group.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
import { ItemCard } from '@components/item-card';
import { ItemCardGroup } from '@components/item-card-group';
import { PressableFeedback } from '@components/pressable-feedback';
import { Button } from '@heroui/react';

function IconBadge({ children }: { children: string }) {
  return (
    <span className="flex size-8 items-center justify-center rounded-md bg-neutral-100 text-xs font-semibold text-neutral-700">
      {children}
    </span>
  );
}

export function Default() {
  return (
    <div className="w-full max-w-[560px]">
      <ItemCardGroup>
        <ItemCardGroup.Header>
          <div>
            <ItemCardGroup.Title>Developer Settings</ItemCardGroup.Title>
            <ItemCardGroup.Description>
              Connected tools for the workspace.
            </ItemCardGroup.Description>
          </div>
        </ItemCardGroup.Header>

        <ItemCard>
          <ItemCard.Icon>
            <IconBadge>GH</IconBadge>
          </ItemCard.Icon>
          <ItemCard.Content>
            <ItemCard.Title>GitHub</ItemCard.Title>
            <ItemCard.Description>
              Connected to the design-system repository.
            </ItemCard.Description>
          </ItemCard.Content>
          <ItemCard.Action>
            <Button size="sm" variant="outline">
              Manage
            </Button>
          </ItemCard.Action>
        </ItemCard>

        <ItemCard>
          <ItemCard.Icon>
            <IconBadge>PR</IconBadge>
          </ItemCard.Icon>
          <ItemCard.Content>
            <ItemCard.Title>Deploy Previews</ItemCard.Title>
            <ItemCard.Description>
              Preview branches are created for every pull request.
            </ItemCard.Description>
          </ItemCard.Content>
          <ItemCard.Action>
            <span className="text-sm text-neutral-500">Open</span>
          </ItemCard.Action>
        </ItemCard>

        <ItemCard<'button'>
          className="relative w-full cursor-pointer overflow-hidden text-left"
          render={(props) => <button type="button" {...props} />}
        >
          <PressableFeedback.Ripple />
          <ItemCard.Icon>
            <IconBadge>SL</IconBadge>
          </ItemCard.Icon>
          <ItemCard.Content>
            <ItemCard.Title>Slack Alerts</ItemCard.Title>
            <ItemCard.Description>
              Send component release notes to the design channel.
            </ItemCard.Description>
          </ItemCard.Content>
          <ItemCard.Action>
            <span className="text-sm text-neutral-500">Configure</span>
          </ItemCard.Action>
        </ItemCard>
      </ItemCardGroup>
    </div>
  );
}
```
