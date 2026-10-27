# Cube Design System


Cube is the design system for BosAgent. This site is the Web reference: live components, generated props, Figma pages, and a changelog built from git history.

The interactive gallery stays at the [Cube preview](https://yuchuanux-a11y.github.io/cube-preview/#PromptInputQueue). Mobile components are shown there, including [Mobile / Button](https://yuchuanux-a11y.github.io/cube-preview/#Mobile/Button), and are not documented on this site.

## How components are imported

Foundation components come from HeroUI v3:

```tsx
import { Button } from "@heroui/react";
```

Cube components come from `@bosagent/cube-ui`. Heavy components use a subpath:

```tsx
import { ActionBar } from "@bosagent/cube-ui";
import { AreaChart } from "@bosagent/cube-ui/area-chart";
```

Load styles in this order: Tailwind CSS, `@heroui/styles`, then `@bosagent/cube-ui/cube`. The theme source is `packages/cube-ui/src/css/cube-contract.css`. Set `data-theme="light"` or `data-theme="dark"` on the document.

## What a component page contains

- A preview that renders the real component.
- A props table generated from the TypeScript type of the root export.
- A Figma link when `data/figma-pages.json` has that component name. Unmatched components do not get a guessed link.

Agent-readable copies are linked from each page and indexed at [/llms.txt](https://yuchuanux-a11y.github.io/cube-preview/docs/llms.txt).

## Updates

[Changelog](https://yuchuanux-a11y.github.io/cube-preview/docs/changelog) is generated from git history at build time. The curated narrative remains `CHANGELOG.md` in the repository.
