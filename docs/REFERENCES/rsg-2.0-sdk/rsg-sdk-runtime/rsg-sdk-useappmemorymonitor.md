---
title: 'useAppMemoryMonitor'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'useAppMemoryMonitor'
  description: 'Returns a reactive accessor for the memory warnings the runtime reports for the app.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-usecec
      title: 'useCec'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#useAppMemoryMonitor.deck -->

Returns a reactive accessor for the memory warnings the runtime reports for the app

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts`. -->

```typescript
import { useAppMemoryMonitor } from "@roku-sdk/runtime/app-memory-monitor";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#useAppMemoryMonitor.signature -->

```typescript
const useAppMemoryMonitor: () => { memoryWarning: Accessor<MemoryStatus | null> } & Record<string, never>
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/app-memory-monitor.ts#useAppMemoryMonitor.description -->

Returns a reactive accessor for the memory warnings the runtime reports for the app.

`memoryWarning` is `null` until the first warning arrives, then holds the latest
`MemoryStatus`, whose `memoryUsagePercent` is the share of the app's memory limit in use. Use it
to free caches or reduce work when memory runs low. Call the hook inside a component; the
warning handler is removed when the last component using it is cleaned up. For one-off memory
queries, use [getAppMemoryMonitor](doc:rsg-sdk-getappmemorymonitor).
