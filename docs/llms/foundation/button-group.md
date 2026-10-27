# ButtonGroup

Group related buttons together with consistent styling and spacing

Foundation component from `@heroui/react`, styled with the Cube theme.

## Import

```tsx
import { ButtonGroup } from "@heroui/react";
```

## Figma

[Open ButtonGroup in Figma](https://www.figma.com/design/D5ZApigd5hFmvI54TkJlAh/Cube-Design-System-for-Web?node-id=14202-4550)

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `fullWidth` | `boolean` | No | `—` | — |
| `orientation` | `"horizontal" \| "vertical"` | No | `—` | The orientation of the button group |
| `size` | `"md" \| "lg" \| "sm"` | No | `—` | — |
| `variant` | `"outline" \| "ghost" \| "danger" \| "danger-soft" \| "primary" \| "secondary" \| "tertiary"` | No | `—` | — |
| `children` | `ChildrenOrFunction<GroupRenderProps>` | No | `—` | The children of the component. A function may be provided to alter the children based on component state. |
| `className` | `ClassNameOrFunction<GroupRenderProps>` | No | `'react-aria-Group'` | The CSS [className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) for the element. A function may be provided to compute the class based on component state. |
| `isDisabled` | `boolean` | No | `—` | Whether the group is disabled. |
| `isInvalid` | `boolean` | No | `—` | Whether the group is invalid. |
| `isReadOnly` | `boolean` | No | `—` | Whether the group is read only. |
| `onHoverChange` | `(isHovering: boolean) => void` | No | `—` | Handler that is called when the hover state changes. |
| `onHoverEnd` | `(e: HoverEvent) => void` | No | `—` | Handler that is called when a hover interaction ends. |
| `onHoverStart` | `(e: HoverEvent) => void` | No | `—` | Handler that is called when a hover interaction starts. |
| `render` | `DOMRenderFunction<"div", GroupRenderProps>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: - You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). - Only a single root DOM element can be rendered (no fragments). - You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `role` | `"group" \| "presentation" \| "region"` | No | `'group'` | An accessibility role for the group. By default, this is set to `'group'`. Use `'region'` when the contents of the group is important enough to be included in the page table of contents. Use `'presentation'` if the group is visual only and does not represent a semantic grouping of controls. |
| `slot` | `string` | No | `—` | A slot name for the component. Slots allow the component to receive props from a parent component. An explicit `null` value indicates that the local props completely override all props received from a parent. |
| `style` | `StyleOrFunction<GroupRenderProps>` | No | `—` | The inline [style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style) for the element. A function may be provided to compute the style based on component state. |

## Parts

- `ButtonGroup.Separator`

## Example source

```tsx
'use client';

import {
  ChevronDown,
  ChevronLeft,
  ChevronRight,
  CodeFork,
  Ellipsis,
  Picture,
  Pin,
  QrCode,
  Star,
  TextAlignCenter,
  TextAlignJustify,
  TextAlignLeft,
  TextAlignRight,
  ThumbsDown,
  ThumbsUp,
  Video,
} from "@gravity-ui/icons";
import {Button, ButtonGroup, Chip, Description, Dropdown, Label} from "@heroui/react";

export function Basic() {
  return (
    <div className="flex flex-col items-start gap-6">
      {/* Single button with dropdown */}
      <div className="flex flex-col gap-2">
        <ButtonGroup>
          <Button>Merge pull request</Button>
          <Dropdown>
            <Button isIconOnly aria-label="More options">
              <ButtonGroup.Separator />
              <ChevronDown />
            </Button>
            <Dropdown.Popover className="max-w-[290px]" placement="bottom end">
              <Dropdown.Menu>
                <Dropdown.Item
                  className="flex flex-col items-start gap-1"
                  id="merge"
                  textValue="Create a merge commit"
                >
                  <Label>Create a merge commit</Label>
                  <Description>
                    All commits from this branch will be added to the base branch
                  </Description>
                </Dropdown.Item>
                <Dropdown.Item
                  className="flex flex-col items-start gap-1"
                  id="squash-and-merge"
                  textValue="Squash and merge"
                >
                  <Label>Squash and merge</Label>
                  <Description>
                    The 14 commits from this branch will be combined into one commit in the base
                    branch
                  </Description>
                </Dropdown.Item>
                <Dropdown.Item
                  className="flex flex-col items-start gap-1"
                  id="rebase-and-merge"
                  textValue="Rebase and merge"
                >
                  <Label>Rebase and merge</Label>
                  <Description>
                    The 14 commits from this branch will be rebased and added to the base branch
                  </Description>
                </Dropdown.Item>
              </Dropdown.Menu>
            </Dropdown.Popover>
          </Dropdown>
        </ButtonGroup>
      </div>

      {/* Individual buttons */}
      <div className="flex flex-col gap-2">
        <div className="flex flex-wrap gap-x-2 gap-y-4">
          <ButtonGroup variant="tertiary">
            <Button>
              <CodeFork className="size-3.5" />
              Fork
              <Chip color="accent" size="sm" variant="soft">
                24
              </Chip>
            </Button>
            <Button isIconOnly aria-label="More fork options">
              <ButtonGroup.Separator />
              <ChevronDown />
            </Button>
          </ButtonGroup>
          <ButtonGroup variant="tertiary">
            <Button isIconOnly aria-label="Show QR code">
              <QrCode />
            </Button>
            <Button>
              <ButtonGroup.Separator />
              Scan to pay
            </Button>
          </ButtonGroup>
          <ButtonGroup variant="tertiary">
            <Button>
              <ThumbsUp />
              <span className="text-xs font-semibold">2.4K</span>
            </Button>
            <Button isIconOnly aria-label="Dislike">
              <ButtonGroup.Separator />
              <ThumbsDown />
            </Button>
          </ButtonGroup>
          <ButtonGroup variant="tertiary">
            <Button>
              <Star className="size-3.5" />
              Star
            </Button>
            <Button className="px-2">
              <ButtonGroup.Separator />
              <Chip color="accent" size="sm" variant="soft">
                104
              </Chip>
            </Button>
          </ButtonGroup>
          <ButtonGroup variant="tertiary">
            <Button>
              <Pin />
              Pinned
            </Button>
            <Button isIconOnly aria-label="More pin options">
              <ButtonGroup.Separator />
              <ChevronDown />
            </Button>
          </ButtonGroup>
        </div>
      </div>

      {/* Previous/Next Button Group */}
      <div className="flex flex-col gap-2">
        <ButtonGroup variant="tertiary">
          <Button>
            <ChevronLeft />
            Previous
          </Button>
          <Button>
            <ButtonGroup.Separator />
            Next
            <ChevronRight />
          </Button>
        </ButtonGroup>
      </div>

      {/* Content Selection Button Group */}
      <div className="flex flex-col gap-2">
        <ButtonGroup variant="tertiary">
          <Button>
            <Picture />
            Photos
          </Button>
          <Button>
            <ButtonGroup.Separator />
            <Video />
            Videos
          </Button>
          <Button isIconOnly aria-label="More options">
            <ButtonGroup.Separator />
            <Ellipsis />
          </Button>
        </ButtonGroup>
      </div>

      {/* Text Alignment Button Group */}
      <div className="flex flex-col gap-2">
        <ButtonGroup variant="tertiary">
          <Button>Left</Button>
          <Button>
            <ButtonGroup.Separator />
            Center
          </Button>
          <Button>
            <ButtonGroup.Separator />
            Right
          </Button>
        </ButtonGroup>
      </div>

      {/* Icon-Only Alignment Button Group */}
      <div className="flex flex-col gap-2">
        <ButtonGroup variant="tertiary">
          <Button isIconOnly aria-label="Align left">
            <TextAlignLeft />
          </Button>
          <Button isIconOnly aria-label="Align center">
            <ButtonGroup.Separator />
            <TextAlignCenter />
          </Button>
          <Button isIconOnly aria-label="Align right">
            <ButtonGroup.Separator />
            <TextAlignRight />
          </Button>
          <Button isIconOnly aria-label="Justify">
            <ButtonGroup.Separator />
            <TextAlignJustify />
          </Button>
        </ButtonGroup>
      </div>
    </div>
  );
}

export { Basic as Preview };
```
