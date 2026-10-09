---
title: 'getRandomValues'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getRandomValues'
  description: 'Web Crypto-compatible getRandomValues: fills the provided typed array with cryptographically secure random bytes and returns it.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getregistry
      title: 'getRegistry'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomValues.deck -->

Web Crypto-compatible `getRandomValues`: fills the provided typed array with cryptographically secure random bytes and returns it

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/crypto.ts`. -->

```typescript
import { getRandomValues } from "@roku-sdk/runtime/crypto";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomValues.signature -->

```typescript
getRandomValues(array: T): T
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomValues.description -->

Web Crypto-compatible `getRandomValues`: fills the provided typed array with
cryptographically secure random bytes and returns it.

## Parameters
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomValues.params -->

| Name | Type | Description |
| :--- | :--- | :--- |
| `array` | `T` | A typed array to fill in place. |

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomValues.returns -->

The same `array` reference, filled with random bytes.
