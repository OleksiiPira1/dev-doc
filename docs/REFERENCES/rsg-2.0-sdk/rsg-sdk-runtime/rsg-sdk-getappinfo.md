---
title: 'getAppInfo'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getAppInfo'
  description: 'Returns the app''s metadata from the runtime, such as its ID, version, title and whether it is a sideloaded developer build.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getappmemorymonitor
      title: 'getAppMemoryMonitor'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/app-info.ts#getAppInfo.deck -->

Returns the app's metadata from the runtime, such as its ID, version, title and whether it is a sideloaded developer build

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/app-info.ts`. -->

```typescript
import { getAppInfo } from "@roku-sdk/runtime/app-info";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/app-info.ts#getAppInfo.signature -->

```typescript
const getAppInfo: () => AppInfo
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/app-info.ts#getAppInfo.description -->

Returns the app's metadata from the runtime, such as its ID, version, title and whether it is a
sideloaded developer build.

This is the TypeScript counterpart of BrightScript's `roAppInfo`. The call is synchronous, and the
runtime object is fetched on the first call and reused afterwards. Use `getManifestValue` on the
result to read any other key from the app's manifest.

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/app-info.ts#getAppInfo.example -->

```ts
const appInfo = getAppInfo();
const label = `${appInfo.title} ${appInfo.version}`;
```
