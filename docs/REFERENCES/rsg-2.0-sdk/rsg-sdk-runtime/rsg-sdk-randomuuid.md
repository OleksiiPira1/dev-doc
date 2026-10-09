---
title: 'randomUUID'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'randomUUID'
  description: 'Generates a version 4 UUID string using DeviceInfo.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-subtle
      title: 'subtle'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#randomUUID.deck -->

Generates a version 4 UUID string using DeviceInfo

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/crypto.ts`. -->

```typescript
import { randomUUID } from "@roku-sdk/runtime/crypto";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#randomUUID.signature -->

```typescript
randomUUID(): string
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#randomUUID.description -->

Generates a version 4 UUID string using DeviceInfo.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#randomUUID.returns -->

A UUID formatted as a lowercase string.
