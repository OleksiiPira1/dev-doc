---
title: 'getAppMemoryMonitor'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getAppMemoryMonitor'
  description: 'Resolves to an object for querying the app''s memory usage and limits.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getaudioguide
      title: 'getAudioGuide'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#getAppMemoryMonitor.deck -->

Resolves to an object for querying the app's memory usage and limits

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts`. -->

```typescript
import { getAppMemoryMonitor } from "@roku-sdk/runtime/app-memory-monitor";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#getAppMemoryMonitor.signature -->

```typescript
getAppMemoryMonitor(): Promise<AppMemoryMonitor>
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#getAppMemoryMonitor.description -->

Resolves to an object for querying the app's memory usage and limits.

This wraps the runtime's app memory monitor, the TypeScript counterpart of BrightScript's
`roAppMemoryMonitor`, and exposes only its query methods. To react to memory warnings, use
[useAppMemoryMonitor](doc:rsg-sdk-useappmemorymonitor) instead.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#getAppMemoryMonitor.returns -->

A promise that resolves to the app's [AppMemoryMonitor](doc:rsg-sdk-getappmemorymonitor#appmemorymonitor).

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#getAppMemoryMonitor.example -->

```ts
const monitor = await getAppMemoryMonitor();
console.log(`Memory used: ${monitor.getMemoryLimitPercent()}%`);
```

## Types
<!-- generator-heading -->

### AppMemoryMonitor
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#AppMemoryMonitor.description -->

The memory queries that [getAppMemoryMonitor](doc:rsg-sdk-getappmemorymonitor) exposes to app code.

Each method reads the current value from the runtime when it is called. Memory warnings are not
part of this object; subscribe to them with [useAppMemoryMonitor](doc:rsg-sdk-useappmemorymonitor).

<!-- derived: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#AppMemoryMonitor.table -->

```typescript
type AppMemoryMonitor = unknown;
```
