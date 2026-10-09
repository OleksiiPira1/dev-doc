---
title: 'getFileSystem'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getFileSystem'
  description: 'Get a FileSystem API object exposing safe file operations.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getfontmeasure
      title: 'getFontMeasure'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/file-system.ts#getFileSystem.deck -->

Get a FileSystem API object exposing safe file operations

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/file-system.ts`. -->

```typescript
import { getFileSystem } from "@roku-sdk/runtime/file-system";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/file-system.ts#getFileSystem.signature -->

```typescript
getFileSystem(): Promise<FileSystemInternal | null>
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/file-system.ts#getFileSystem.description -->

Get a FileSystem API object exposing safe file operations.

This wraps the runtime file system instance to only provide the approved
method set that is safe for consumer use.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/file-system.ts#getFileSystem.returns -->

Promise resolved with `FileSystemInternal` wrapper object.

## Types
<!-- generator-heading -->

### FileSystemInternal
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/file-system.ts#FileSystemInternal.description -->

Safe interface for file system access exposed to app code.

This intentionally excludes internal runtime-only methods such as
`setStorageDeviceChangeHandler` to enforce a safer operation surface.

<!-- derived: rsg-sdk/external/packages/runtime/src/file-system.ts#FileSystemInternal.table -->

```typescript
type FileSystemInternal = Omit<FileSystem, "setStorageDeviceChangeHandler" | "apiVersion">;
```
