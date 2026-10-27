# DropZone

Cube component `DropZone` from `@bosagent/cube-ui/drop-zone`.

| 项目 | 内容 |
| --- | --- |
| 包 | `@bosagent/cube-ui/drop-zone` |
| 分层 | Cube |
| 成熟度 | 代码可预览。设计 registry 没有该组件的规范条目（建设中）。 |
| 稳定 ID | 未登记 |
| 源码 | `packages/cube-ui/src/components/drop-zone` |

检索：DropZone、drop-zone。

## Import

```tsx
import { DropZone } from "@bosagent/cube-ui/drop-zone";
import { DropZone } from "@bosagent/cube-ui";
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
| `className` | `string` | No | `—` | — |
| `render` | `DOMRenderFunction<E, undefined>` | No | `—` | Overrides the default DOM element with a custom render function. This allows rendering existing components with built-in styles and behaviors such as router links, animation libraries, and pre-styled components. Requirements: * You must render the expected element type (e.g. if `<button>` is expected, you cannot render an `<a>`). * Only a single root DOM element can be rendered (no fragments). * You must pass through props and ref to the underlying DOM element, merging with your own prop as appropriate. |
| `slot` | `JSX.IntrinsicElements[E]["slot"]` | No | `—` | — |

## Parts

- `DropZone.Area`
- `DropZone.Description`
- `DropZone.FileFormatIcon`
- `DropZone.FileInfo`
- `DropZone.FileItem`
- `DropZone.FileList`
- `DropZone.FileMeta`
- `DropZone.FileName`
- `DropZone.FileProgress`
- `DropZone.FileProgressFill`
- `DropZone.FileProgressTrack`
- `DropZone.FileRemoveTrigger`
- `DropZone.FileRetryTrigger`
- `DropZone.Icon`
- `DropZone.Input`
- `DropZone.Label`
- `DropZone.Trigger`

## Token

主题值见 [设计基础](/foundations)、[色彩](/foundations/color)、[圆角](/foundations/radius)、[阴影](/foundations/shadow)。

组件级 token 对照建设中。

## 画廊

[DropZone](https://yuchuanux-a11y.github.io/cube-preview/#DropZone)

公开画廊的 Web Demo。哈希是示例目录里的组件名。

[Markdown for agents](https://yuchuanux-a11y.github.io/cube-preview/docs-preview/llms/cube/drop-zone.md)

## Example source

Demo files may import `@components/...`. Apps should use the package path in Import.

```tsx
'use client';

import { useCallback, useEffect, useRef, useState } from 'react';
import { DropZone } from '@components/drop-zone';

interface UploadFile {
  id: string;
  name: string;
  size: number;
  status: 'uploading' | 'complete' | 'failed';
  progress: number;
}

function formatFileSize(bytes: number): string {
  if (bytes < 1024) return `${bytes} B`;
  if (bytes < 1024 * 1024) return `${(bytes / 1024).toFixed(0)} KB`;

  return `${(bytes / (1024 * 1024)).toFixed(1)} MB`;
}

function getExtension(name: string): string {
  const dot = name.lastIndexOf('.');

  return dot > 0 ? name.slice(dot + 1) : '';
}

type FileFormatColor = 'blue' | 'gray' | 'green' | 'orange' | 'purple' | 'red';

function getFormatColor(ext: string): FileFormatColor {
  const map: Record<string, FileFormatColor> = {
    csv: 'green',
    doc: 'blue',
    docx: 'blue',
    fig: 'purple',
    jpeg: 'blue',
    jpg: 'blue',
    json: 'orange',
    mp4: 'purple',
    pdf: 'red',
    png: 'green',
    svg: 'green',
    ts: 'blue',
    tsx: 'blue',
    txt: 'gray',
    xlsx: 'green',
    zip: 'orange',
  };

  return map[ext.toLowerCase()] ?? 'gray';
}

export function Default() {
  const [files, setFiles] = useState<UploadFile[]>([]);
  const timersRef = useRef<Map<string, ReturnType<typeof setInterval>>>(
    new Map()
  );

  useEffect(() => {
    files.forEach((file) => {
      if (file.status === 'uploading' && !timersRef.current.has(file.id)) {
        const fileId = file.id;
        const timer = setInterval(() => {
          setFiles((prev) =>
            prev.map((f) => {
              if (f.id !== fileId || f.status !== 'uploading') return f;
              const next = Math.min(
                f.progress + Math.floor(Math.random() * 12) + 3,
                100
              );

              if (next >= 100) {
                const t = timersRef.current.get(fileId);

                if (t) clearInterval(t);
                timersRef.current.delete(fileId);

                return { ...f, progress: 100, status: 'complete' as const };
              }

              return { ...f, progress: next };
            })
          );
        }, 350);

        timersRef.current.set(fileId, timer);
      }
    });
  }, [files]);

  useEffect(() => {
    const ref = timersRef.current;

    return () => {
      ref.forEach((timer) => clearInterval(timer));
      ref.clear();
    };
  }, []);

  const handleSelect = useCallback((fileList: FileList) => {
    const newFiles: UploadFile[] = Array.from(fileList).map((f, i) => ({
      id: `${Date.now()}-${i}`,
      name: f.name,
      progress: 0,
      size: f.size,
      status: 'uploading' as const,
    }));

    setFiles((prev) => [...newFiles, ...prev]);
  }, []);

  const handleDrop = useCallback(
    async (e: {
      items: Array<{ kind: string; getFile?: () => Promise<File> }>;
    }) => {
      const dropped: File[] = [];

      for (const item of e.items) {
        if (item.kind === 'file' && item.getFile) {
          dropped.push(await item.getFile());
        }
      }

      const newFiles: UploadFile[] = dropped.map((f, i) => ({
        id: `${Date.now()}-${i}`,
        name: f.name,
        progress: 0,
        size: f.size,
        status: 'uploading' as const,
      }));

      setFiles((prev) => [...newFiles, ...prev]);
    },
    []
  );

  const handleRemove = useCallback((id: string) => {
    setFiles((prev) => prev.filter((f) => f.id !== id));
    const timer = timersRef.current.get(id);

    if (timer) {
      clearInterval(timer);
      timersRef.current.delete(id);
    }
  }, []);

  return (
    <DropZone className="w-[420px]">
      <DropZone.Area onDrop={handleDrop as any}>
        <DropZone.Icon />
        <DropZone.Label>Drag files here or click to browse</DropZone.Label>
        <DropZone.Description>
          Supports JPEG, PNG, PDF, and MP4 up to 50 MB.
        </DropZone.Description>
        <DropZone.Trigger>Select File</DropZone.Trigger>
      </DropZone.Area>
      <DropZone.Input onSelect={handleSelect} />

      {files.length > 0 && (
        <DropZone.FileList>
          {files.map((file) => {
            const ext = getExtension(file.name).toUpperCase();

            return (
              <DropZone.FileItem key={file.id} status={file.status}>
                <DropZone.FileFormatIcon
                  color={getFormatColor(ext.toLowerCase())}
                  format={ext}
                />
                <DropZone.FileInfo>
                  <DropZone.FileName>{file.name}</DropZone.FileName>
                  <DropZone.FileMeta>
                    {formatFileSize(file.size)}
                    {file.status === 'uploading' && ` | ${file.progress}%`}
                    {file.status === 'complete' && (
                      <span className="text-success"> | 100%</span>
                    )}
                  </DropZone.FileMeta>
                  {file.status === 'uploading' && (
                    <DropZone.FileProgress value={file.progress}>
                      <DropZone.FileProgressTrack>
                        <DropZone.FileProgressFill />
                      </DropZone.FileProgressTrack>
                    </DropZone.FileProgress>
                  )}
                </DropZone.FileInfo>
                <DropZone.FileRemoveTrigger
                  aria-label={`Remove ${file.name}`}
                  onPress={() => handleRemove(file.id)}
                />
              </DropZone.FileItem>
            );
          })}
        </DropZone.FileList>
      )}
    </DropZone>
  );
}
```
