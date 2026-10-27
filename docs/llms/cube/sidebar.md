# Sidebar

Cube component `Sidebar` from `@bosagent/cube-ui/sidebar`.

Cube component. Source: `packages/cube-ui/src/components/sidebar`.

## Import

```tsx
import { Sidebar } from "@bosagent/cube-ui/sidebar";
import { Sidebar } from "@bosagent/cube-ui";
```

## Preview

The docs page renders a live preview of the real component.

## Props

Generated from the TypeScript type of the root export. DOM attributes inherited from React are omitted.

| Prop | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `children` | `React.ReactNode` | Yes | `—` | — |
| `className` | `string` | No | `—` | — |
| `slot` | `string` | No | `—` | — |

## Parts

- `Sidebar.Content`
- `Sidebar.Footer`
- `Sidebar.Group`
- `Sidebar.GroupLabel`
- `Sidebar.Header`
- `Sidebar.Main`
- `Sidebar.Menu`
- `Sidebar.MenuAction`
- `Sidebar.MenuActions`
- `Sidebar.MenuChip`
- `Sidebar.MenuHeader`
- `Sidebar.MenuIcon`
- `Sidebar.MenuIndicator`
- `Sidebar.MenuItem`
- `Sidebar.MenuItemContent`
- `Sidebar.MenuLabel`
- `Sidebar.MenuSection`
- `Sidebar.MenuTrigger`
- `Sidebar.Mobile`
- `Sidebar.Page`
- `Sidebar.Pages`
- `Sidebar.Provider`
- `Sidebar.Rail`
- `Sidebar.Separator`
- `Sidebar.Submenu`
- `Sidebar.Tooltip`
- `Sidebar.Trigger`

## Example source

```tsx
'use client';

import type { ReactNode } from 'react';
import { Sidebar } from '@bosagent/cube-ui';
import {
  ArrowRightFromSquare,
  Bell,
  ChartColumn,
  CircleQuestion,
  Copy,
  EllipsisVertical,
  FolderOpen,
  Gear,
  House,
  ListCheck,
  TrashBin,
} from '@gravity-ui/icons';
import { Breadcrumbs, Chip, Dropdown, Label } from '@heroui/react';
const sidebarBrandName = 'HeroUI';

const nestedNavItems = [
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

const SidebarStoryHeader = ({
  items,
}: {
  items: Array<{
    icon?: ReactNode;
    label: string;
  }>;
}) => (
  <div className="flex items-center gap-3 p-4">
    <Sidebar.Trigger />
    <Breadcrumbs className="min-w-0">
      {items.map((item, index) => {
        const isLast = index === items.length - 1;

        return (
          <Breadcrumbs.Item
            key={`${item.label}-${index}`}
            className={`min-w-0 ${isLast ? 'font-semibold' : 'text-muted'}`}
            href={isLast ? undefined : '#'}
          >
            <span className="flex min-w-0 items-center gap-2 overflow-hidden">
              {item.icon}
              <span className="truncate">{item.label}</span>
            </span>
          </Breadcrumbs.Item>
        );
      })}
    </Breadcrumbs>
  </div>
);

const SidebarItemActions = ({ label }: { label: string }) => (
  <Dropdown>
    <Dropdown.Trigger
      aria-label={`More actions for ${label}`}
      className="sidebar__menu-action"
      data-slot="sidebar-menu-action"
    >
      <EllipsisVertical className="size-4" />
    </Dropdown.Trigger>
    <Dropdown.Popover className="w-44" offset={6} placement="right top">
      <Dropdown.Menu aria-label={`${label} actions`}>
        <Dropdown.Item id="open" textValue="Open">
          <FolderOpen className="size-4 shrink-0 text-muted" />
          <Label>Open</Label>
        </Dropdown.Item>
        <Dropdown.Item id="duplicate" textValue="Duplicate">
          <Copy className="size-4 shrink-0 text-muted" />
          <Label>Duplicate</Label>
        </Dropdown.Item>
        <Dropdown.Item id="delete" textValue="Delete" variant="danger">
          <TrashBin className="size-4 shrink-0 text-danger" />
          <Label>Delete</Label>
        </Dropdown.Item>
      </Dropdown.Menu>
    </Dropdown.Popover>
  </Dropdown>
);

export function Default() {
  return (
    <div className="sidebar-demo-frame">
      <Sidebar.Provider>
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
                {sidebarBrandName}
              </span>
            </div>
          </Sidebar.Header>
          <Sidebar.Content>
            <Sidebar.Group>
              <Sidebar.Menu
                aria-label="Navigation"
                defaultExpandedKeys={['Analytics']}
              >
                {nestedNavItems.map((item) => (
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
                            <Sidebar.MenuActions className="ml-auto">
                              <SidebarItemActions label={subitem} />
                            </Sidebar.MenuActions>
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
              <Sidebar.MenuItem
                href="#"
                id="help"
                textValue="Help & Information"
              >
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
                {sidebarBrandName}
              </span>
            </div>
          </Sidebar.Header>
          <Sidebar.Content>
            <Sidebar.Group>
              <Sidebar.Menu
                aria-label="Navigation"
                defaultExpandedKeys={['Analytics']}
              >
                {nestedNavItems.map((item) => (
                  <Sidebar.MenuItem
                    key={item.label}
                    href={item.items ? undefined : '#'}
                    id={item.label}
                    textValue={item.label}
                  >
                    <Sidebar.MenuIcon>
                      <item.icon className="size-4" />
                    </Sidebar.MenuIcon>
                    <Sidebar.MenuLabel>{item.label}</Sidebar.MenuLabel>
                    {item.badge ? (
                      <Sidebar.MenuChip>
                        <Chip color="success" size="sm" variant="soft">
                          {item.badge}
                        </Chip>
                      </Sidebar.MenuChip>
                    ) : null}
                    {!item.items && !item.badge ? (
                      <Sidebar.MenuActions className="ml-auto">
                        <Sidebar.MenuAction aria-label={`Notify ${item.label}`}>
                          <Bell className="size-4" />
                        </Sidebar.MenuAction>
                        <SidebarItemActions label={item.label} />
                      </Sidebar.MenuActions>
                    ) : null}
                    {item.items ? (
                      <>
                        <Sidebar.MenuTrigger>
                          <Sidebar.MenuIndicator />
                        </Sidebar.MenuTrigger>
                        <Sidebar.Submenu>
                          {item.items.map((subitem) => (
                            <Sidebar.MenuItem
                              key={subitem}
                              href="#"
                              id={`${item.label}-${subitem}`}
                              textValue={subitem}
                            >
                              <Sidebar.MenuLabel>{subitem}</Sidebar.MenuLabel>
                              <Sidebar.MenuActions className="ml-auto">
                                <SidebarItemActions label={subitem} />
                              </Sidebar.MenuActions>
                            </Sidebar.MenuItem>
                          ))}
                        </Sidebar.Submenu>
                      </>
                    ) : null}
                  </Sidebar.MenuItem>
                ))}
              </Sidebar.Menu>
            </Sidebar.Group>
          </Sidebar.Content>
        </Sidebar.Mobile>
        <Sidebar.Main>
          <SidebarStoryHeader
            items={[{ icon: <House className="size-4" />, label: 'Dashboard' }]}
          />
          <div className="p-6">
            <p className="text-muted">
              Main content area. Resize to mobile to see the Sheet sidebar.
            </p>
          </div>
        </Sidebar.Main>
      </Sidebar.Provider>
    </div>
  );
}
```
