---
title: 'getRandomBytes'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getRandomBytes'
  description: 'Returns an ArrayBuffer containing length cryptographically secure random bytes.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getrandomvalues
      title: 'getRandomValues'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomBytes.deck -->

Returns an ArrayBuffer containing `length` cryptographically secure random bytes

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/crypto.ts`. -->

```typescript
import { getRandomBytes } from "@roku-sdk/runtime/crypto";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomBytes.signature -->

```typescript
getRandomBytes(length: number): ArrayBuffer
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomBytes.description -->

Returns an ArrayBuffer containing `length` cryptographically secure random bytes.

Backed by the Roku runtime's global `crypto.getRandomBytes()` host function,
which uses OpenSSL's RAND_bytes() (HW-backed CSPRNG via /dev/urandom).

## Parameters
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomBytes.params -->

| Name | Type | Description |
| :--- | :--- | :--- |
| `length` | `number` | Number of bytes to generate. Must be a non-negative integer   no greater than 65536. |

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#getRandomBytes.returns -->

An ArrayBuffer of `length` random bytes.
