# AppLayout

Cube component `AppLayout` from `@bosagent/cube-ui/app-layout`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/app-layout` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/app-layout` |

检索：AppLayout、app-layout。

## Import

```tsx
import { AppLayout } from "@bosagent/cube-ui/app-layout";
import { AppLayout } from "@bosagent/cube-ui";
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
| `children` | `React.ReactNode` | Yes | `—` | — |
| `aside` | `React.ReactNode` | No | `—` | — |
| `asideDefaultSize` | `ResizableSize` | No | `20` | Default size of the aside when resizable. Numbers are percentages; strings accept CSS units. |
| `asideMaxSize` | `ResizableSize` | No | `40` | Max aside size when resizable. Numbers are percentages; strings accept CSS units. |
| `asideMinSize` | `ResizableSize` | No | `15` | Min aside size when resizable. Numbers are percentages; strings accept CSS units. |
| `asideMobile` | `"hidden" \| "sheet"` | No | `—` | — |
| `asideOpen` | `boolean` | No | `—` | — |
| `asideResizable` | `boolean` | No | `—` | — |
| `asideResizeBehavior` | `ResizablePanelGroupResizeBehavior` | No | `"preserve-relative-size"` | How the aside panel behaves when the layout width changes. |
| `asideToggleShortcut` | `string \| false` | No | `—` | — |
| `className` | `string` | No | `—` | — |
| `defaultAsideOpen` | `boolean` | No | `—` | — |
| `defaultSidebarOpen` | `boolean` | No | `—` | — |
| `footer` | `React.ReactNode` | No | `—` | — |
| `navbar` | `React.ReactNode` | No | `—` | — |
| `navigate` | `SidebarNavigate` | No | `—` | — |
| `onAsideOpenChange` | `(open: boolean) => void` | No | `—` | — |
| `onSidebarOpenChange` | `(open: boolean) => void` | No | `—` | — |
| `reduceMotion` | `boolean` | No | `—` | — |
| `resizableAutoSaveId` | `string` | No | `—` | — |
| `scrollMode` | `AppLayoutScrollMode` | No | `—` | — |
| `sidebar` | `React.ReactNode` | No | `—` | — |
| `sidebarCollapsible` | `"none" \| "icon" \| "offcanvas"` | No | `—` | — |
| `sidebarDefaultSize` | `ResizableSize` | No | `18` | Default size of the sidebar when resizable. Numbers are percentages; strings accept CSS units. |
| `sidebarMaxSize` | `ResizableSize` | No | `30` | Max sidebar size when resizable. Numbers are percentages; strings accept CSS units. |
| `sidebarMinSize` | `ResizableSize` | No | `12` | Min sidebar size when resizable. Numbers are percentages; strings accept CSS units. |
| `sidebarOpen` | `boolean` | No | `—` | — |
| `sidebarResizable` | `boolean` | No | `—` | — |
| `sidebarResizeBehavior` | `ResizablePanelGroupResizeBehavior` | No | `"preserve-relative-size"` | How the sidebar panel behaves when the layout width changes. |
| `sidebarSide` | `"left" \| "right"` | No | `—` | — |
| `sidebarVariant` | `"inset" \| "sidebar" \| "floating"` | No | `—` | — |
| `style` | `React.CSSProperties` | No | `—` | — |
| `toggleShortcut` | `string \| false` | No | `—` | — |
| `toolbar` | `React.ReactNode` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `AppLayout.AsideTrigger`
- `AppLayout.MenuToggle`
- `AppLayout.MobileAside`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[AppLayout](https://yuchuanux-a11y.github.io/cube-preview/#AppLayout)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/app-layout.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { AppLayout } from '@components/app-layout';
import { Navbar } from '@components/navbar';
import { Sidebar } from '@components/sidebar';
import {
  ArrowRightFromSquare,
  Bell,
  ChartColumn,
  CircleQuestion,
  Gear,
  House,
  ListCheck,
  Magnifier,
  Person,
} from '@gravity-ui/icons';
import {
  Avatar,
  Breadcrumbs,
  Button,
  Chip,
  Dropdown,
  Label,
  Separator,
} from '@heroui/react';

export function Default() {
  return (
    <AppLayout
      navbar={<DemoNavbar />}
      sidebar={<DemoSidebar />}
      sidebarCollapsible="offcanvas"
      sidebarDefaultSize="260px"
      sidebarMaxSize="340px"
      sidebarMinSize="220px"
      sidebarResizable
    >
      <div className="p-6">
        <h1 className="text-xl font-semibold text-foreground">Dashboard</h1>
        <p className="mt-2 text-sm text-muted">
          The sidebar fills the full viewport height while the navbar and main
          content live in the right column. Resize to mobile to see the sidebar
          collapse into a sheet.
        </p>
      </div>
    </AppLayout>
  );
}

const BreadcrumbItems = [
  { icon: <House className="size-4" />, label: 'Dashboard' },
];

const navItems = [
  { icon: House, label: 'Dashboard' },
  {
    icon: ChartColumn,
    items: ['Overview', 'Reports', 'Conversions'],
    label: 'Analytics',
  },
  { badge: 'New', icon: ListCheck, label: 'Tracker' },
  {
    icon: Gear,
    items: ['General', 'Team', 'Notifications'],
    label: 'Settings',
  },
];

function DemoSidebar() {
  return (
    <>
      <Sidebar>
        <Sidebar.Header>
          <div className="flex items-center gap-3 px-1 py-2">
            <div className="flex size-6 shrink-0 items-center justify-center rounded-md bg-accent">
              <span className="text-sm font-bold text-white">H</span>
            </div>
            <span
              className="text-sm font-semibold text-foreground"
              data-sidebar="label"
            >
              HeroUI
            </span>
          </div>
        </Sidebar.Header>
        <Sidebar.Content>
          <Sidebar.Group>
            <Sidebar.Menu
              aria-label="Navigation"
              defaultExpandedKeys={['Analytics']}
            >
              {navItems.map((item) => (
                <Sidebar.MenuItem
                  key={item.label}
                  href={item.items ? undefined : '#'}
                  id={item.label}
                  isCurrent={item.label === 'Dashboard'}
                  textValue={item.label}
                >
                  <Sidebar.MenuIcon>
                    <item.icon className="size-4" />
                  </Sidebar.MenuIcon>
                  <Sidebar.MenuLabel>
                    {item.label}
                    {item.items ? (
                      <Sidebar.MenuTrigger>
                        <Sidebar.MenuIndicator />
                      </Sidebar.MenuTrigger>
                    ) : null}
                  </Sidebar.MenuLabel>
                  {item.badge ? (
                    <Sidebar.MenuChip>
                      <Chip color="success" size="sm" variant="soft">
                        {item.badge}
                      </Chip>
                    </Sidebar.MenuChip>
                  ) : null}
                  {item.items ? (
                    <Sidebar.Submenu>
                      {item.items.map((subitem) => (
                        <Sidebar.MenuItem
                          key={subitem}
                          href="#"
                          id={`${item.label}-${subitem}`}
                          textValue={subitem}
                        >
                          <Sidebar.MenuLabel>{subitem}</Sidebar.MenuLabel>
                        </Sidebar.MenuItem>
                      ))}
                    </Sidebar.Submenu>
                  ) : null}
                </Sidebar.MenuItem>
              ))}
            </Sidebar.Menu>
          </Sidebar.Group>
        </Sidebar.Content>
        <Sidebar.Footer>
          <Sidebar.Menu aria-label="Footer actions">
            <Sidebar.MenuItem href="#" id="help" textValue="Help & Information">
              <Sidebar.MenuIcon>
                <CircleQuestion className="size-4" />
              </Sidebar.MenuIcon>
              <Sidebar.MenuLabel>Help & Information</Sidebar.MenuLabel>
            </Sidebar.MenuItem>
            <Sidebar.MenuItem href="#" id="logout" textValue="Log out">
              <Sidebar.MenuIcon>
                <ArrowRightFromSquare className="size-4" />
              </Sidebar.MenuIcon>
              <Sidebar.MenuLabel>Log out</Sidebar.MenuLabel>
            </Sidebar.MenuItem>
          </Sidebar.Menu>
        </Sidebar.Footer>
        <Sidebar.Rail />
      </Sidebar>
      <Sidebar.Mobile>
        <Sidebar.Header>
          <div className="flex items-center gap-3 px-1 py-2">
            <div className="flex size-6 shrink-0 items-center justify-center rounded-md bg-accent">
              <span className="text-sm font-bold text-white">H</span>
            </div>
            <span className="text-sm font-semibold text-foreground">
              HeroUI
            </span>
          </div>
        </Sidebar.Header>
        <Sidebar.Content>
          <Sidebar.Group>
            <Sidebar.Menu
              aria-label="Navigation"
              defaultExpandedKeys={['Analytics']}
            >
              {navItems.map((item) => (
                <Sidebar.MenuItem
                  key={item.label}
                  href={item.items ? undefined : '#'}
                  id={item.label}
                  textValue={item.label}
                >
                  <Sidebar.MenuIcon>
                    <item.icon className="size-4" />
                  </Sidebar.MenuIcon>
                  <Sidebar.MenuLabel>
                    {item.label}
                    {item.items ? (
                      <Sidebar.MenuTrigger>
                        <Sidebar.MenuIndicator />
                      </Sidebar.MenuTrigger>
                    ) : null}
                  </Sidebar.MenuLabel>
                  {item.badge ? (
                    <Sidebar.MenuChip>
                      <Chip color="success" size="sm" variant="soft">
                        {item.badge}
                      </Chip>
                    </Sidebar.MenuChip>
                  ) : null}
                  {item.items ? (
                    <Sidebar.Submenu>
                      {item.items.map((subitem) => (
                        <Sidebar.MenuItem
                          key={subitem}
                          href="#"
                          id={`${item.label}-${subitem}`}
                          textValue={subitem}
                        >
                          <Sidebar.MenuLabel>{subitem}</Sidebar.MenuLabel>
                        </Sidebar.MenuItem>
                      ))}
                    </Sidebar.Submenu>
                  ) : null}
                </Sidebar.MenuItem>
              ))}
            </Sidebar.Menu>
          </Sidebar.Group>
        </Sidebar.Content>
      </Sidebar.Mobile>
    </>
  );
}

function DemoNavbar() {
  return (
    <Navbar maxWidth="full">
      <Navbar.Header>
        <AppLayout.MenuToggle />
        <Sidebar.Trigger />
        <Breadcrumbs className="min-w-0">
          {BreadcrumbItems.map((item, index) => (
            <Breadcrumbs.Item
              key={`${item.label}-${index}`}
              className="min-w-0 font-semibold"
            >
              <span className="flex min-w-0 items-center gap-2 overflow-hidden">
                {item.icon}
                <span className="truncate">{item.label}</span>
              </span>
            </Breadcrumbs.Item>
          ))}
        </Breadcrumbs>
        <Navbar.Spacer />
        <Navbar.Content>
          <Navbar.Item aria-label="Search">
            <Magnifier className="size-4" />
          </Navbar.Item>
          <Navbar.Item aria-label="Notifications">
            <Bell className="size-4" />
          </Navbar.Item>
          <Navbar.Separator />
          <Dropdown>
            <Button isIconOnly aria-label="Account menu" variant="ghost">
              <Avatar className="size-6" color="success" variant="soft">
                <Avatar.Fallback className="text-xs font-semibold">
                  JG
                </Avatar.Fallback>
              </Avatar>
            </Button>
            <Dropdown.Popover className="min-w-[200px]" placement="bottom end">
              <Dropdown.Menu>
                <Dropdown.Item id="account" textValue="Account">
                  <Person className="size-4 text-muted" />
                  <Label>Account</Label>
                </Dropdown.Item>
                <Dropdown.Item id="settings" textValue="Settings">
                  <Gear className="size-4 text-muted" />
                  <Label>Settings</Label>
                </Dropdown.Item>
                <Separator />
                <Dropdown.Item id="sign-out" textValue="Log out">
                  <ArrowRightFromSquare className="size-4 text-muted" />
                  <Label>Log out</Label>
                </Dropdown.Item>
              </Dropdown.Menu>
            </Dropdown.Popover>
          </Dropdown>
        </Navbar.Content>
      </Navbar.Header>
    </Navbar>
  );
}
```
