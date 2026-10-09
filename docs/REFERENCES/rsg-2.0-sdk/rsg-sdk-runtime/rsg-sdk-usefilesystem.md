---
title: 'useFileSystem'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'useFileSystem'
  description: 'Hook for file system storage events for runtime signal-aware components.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-usehdmistatus
      title: 'useHdmiStatus'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/file-system.ts#useFileSystem.deck -->

Hook for file system storage events for runtime signal-aware components

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/file-system.ts`. -->

```typescript
import { useFileSystem } from "@roku-sdk/runtime/file-system";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/file-system.ts#useFileSystem.signature -->

```typescript
const useFileSystem: () => { storageDeviceChanged: Accessor<StorageEvent | null> } & Record<string, never>
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/file-system.ts#useFileSystem.description -->

Hook for file system storage events for runtime signal-aware components.

Provides `storageDeviceChanged` signal that emits a `StorageEvent` whenever
the filesystem device list changes.
