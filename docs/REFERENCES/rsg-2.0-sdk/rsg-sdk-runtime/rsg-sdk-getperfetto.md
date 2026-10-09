---
title: 'getPerfetto'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getPerfetto'
  description: 'Returns the runtime''s Perfetto tracing API, for adding your own events to a performance trace.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getrandombytes
      title: 'getRandomBytes'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/perfetto.ts#getPerfetto.deck -->

Returns the runtime's Perfetto tracing API, for adding your own events to a performance trace

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/perfetto.ts`. -->

```typescript
import { getPerfetto } from "@roku-sdk/runtime/perfetto";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/perfetto.ts#getPerfetto.signature -->

```typescript
getPerfetto(): Perfetto
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/perfetto.ts#getPerfetto.description -->

Returns the runtime's Perfetto tracing API, for adding your own events to a performance trace.

Use it to mark the start and end of work, or a single instant, so that it appears in the
Perfetto trace viewer. On devices whose runtime has no Perfetto support, it returns an object
whose methods do nothing, so tracing calls can stay in the app.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/perfetto.ts#getPerfetto.returns -->

The runtime's `Perfetto` object, or a no-op stand-in when tracing is unavailable.

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/perfetto.ts#getPerfetto.example -->

```ts
const perfetto = getPerfetto();
perfetto.beginEvent("load-catalog");
await loadCatalog();
perfetto.endEvent();
```
