---
title: 'getRegistry'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getRegistry'
  description: 'Resolves to the device registry, the app''s persistent key-value storage.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getsignalbeacon
      title: 'getSignalBeacon'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/registry.ts#getRegistry.deck -->

Resolves to the device registry, the app's persistent key-value storage

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/registry.ts`. -->

```typescript
import { getRegistry } from "@roku-sdk/runtime/registry";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/registry.ts#getRegistry.signature -->

```typescript
const getRegistry: () => Promise<Registry>
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/registry.ts#getRegistry.description -->

Resolves to the device registry, the app's persistent key-value storage.

This is the TypeScript counterpart of BrightScript's `roRegistry`. Data is grouped into named
sections of string keys and values, and it persists across app launches and device reboots.
Use it for small settings such as preferences or sign-in state. Writes can be buffered, so call
`flush()` after important changes.

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/registry.ts#getRegistry.example -->

```ts
const registry = await getRegistry();
registry.create("settings").write("theme", "dark");
await registry.flush();
```
