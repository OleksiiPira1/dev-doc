---
title: 'crypto'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'crypto'
  description: 'Runtime-compatible crypto shim exposing a subset of the Web Crypto API.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-device-info
      title: 'Device info'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#crypto.deck -->

Runtime-compatible crypto shim exposing a subset of the Web Crypto API

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/crypto.ts`. -->

```typescript
import { crypto } from "@roku-sdk/runtime/crypto";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#crypto.signature -->

```typescript
const crypto: { getRandomBytes: (length: number) => ArrayBuffer; getRandomValues: (array: T) => T; randomUUID: () => string; subtle: { decrypt: (algorithm: AlgorithmIdentifier, key: CryptoKey, data: ArrayBuffer) => Promise<ArrayBuffer>; deriveBits: (algorithm: AlgorithmIdentifier, baseKey: CryptoKey, length: number) => Promise<ArrayBuffer>; deriveKey: (algorithm: AlgorithmIdentifier, baseKey: CryptoKey, derivedKeyType: AlgorithmIdentifier | AesKeyGenParams | HmacKeyGenParams, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey>; digest: (algorithm: AlgorithmIdentifier, data: ArrayBuffer) => Promise<ArrayBuffer>; encrypt: (algorithm: AlgorithmIdentifier, key: CryptoKey, data: ArrayBuffer) => Promise<ArrayBuffer>; exportKey: (format: "raw" | "spki" | "pkcs8" | "jwk", key: CryptoKey) => Promise<ArrayBuffer | JsonWebKey>; generateKey: (algorithm: AlgorithmIdentifier, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey | CryptoKeyPair>; importKey: (format: "raw" | "spki" | "pkcs8" | "jwk", keyData: ArrayBuffer | JsonWebKey, algorithm: AlgorithmIdentifier, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey>; sign: (algorithm: AlgorithmIdentifier, key: CryptoKey, data: ArrayBuffer) => Promise<ArrayBuffer>; unwrapKey: (format: "raw" | "spki" | "pkcs8" | "jwk", wrappedKey: ArrayBuffer, unwrappingKey: CryptoKey, unwrapAlgorithm: AlgorithmIdentifier, unwrappedKeyAlgorithm: AlgorithmIdentifier, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey>; verify: (algorithm: AlgorithmIdentifier, key: CryptoKey, signature: ArrayBuffer, data: ArrayBuffer) => Promise<boolean>; wrapKey: (format: "raw" | "spki" | "pkcs8" | "jwk", key: CryptoKey, wrappingKey: CryptoKey, wrapAlgorithm: AlgorithmIdentifier) => Promise<ArrayBuffer> } }
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#crypto.description -->

Runtime-compatible crypto shim exposing a subset of the Web Crypto API.
