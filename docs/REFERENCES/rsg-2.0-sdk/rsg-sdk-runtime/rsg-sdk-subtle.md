---
title: 'subtle'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'subtle'
  description: 'The app''s Web Crypto SubtleCrypto object, backed by the Roku runtime''s crypto support.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-useappmemorymonitor
      title: 'useAppMemoryMonitor'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#subtle.deck -->

The app's Web Crypto `SubtleCrypto` object, backed by the Roku runtime's crypto support

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/crypto.ts`. -->

```typescript
import { subtle } from "@roku-sdk/runtime/crypto";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#subtle.signature -->

```typescript
const subtle: { decrypt: (algorithm: AlgorithmIdentifier, key: CryptoKey, data: ArrayBuffer) => Promise<ArrayBuffer>; deriveBits: (algorithm: AlgorithmIdentifier, baseKey: CryptoKey, length: number) => Promise<ArrayBuffer>; deriveKey: (algorithm: AlgorithmIdentifier, baseKey: CryptoKey, derivedKeyType: AlgorithmIdentifier | AesKeyGenParams | HmacKeyGenParams, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey>; digest: (algorithm: AlgorithmIdentifier, data: ArrayBuffer) => Promise<ArrayBuffer>; encrypt: (algorithm: AlgorithmIdentifier, key: CryptoKey, data: ArrayBuffer) => Promise<ArrayBuffer>; exportKey: (format: "raw" | "spki" | "pkcs8" | "jwk", key: CryptoKey) => Promise<ArrayBuffer | JsonWebKey>; generateKey: (algorithm: AlgorithmIdentifier, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey | CryptoKeyPair>; importKey: (format: "raw" | "spki" | "pkcs8" | "jwk", keyData: ArrayBuffer | JsonWebKey, algorithm: AlgorithmIdentifier, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey>; sign: (algorithm: AlgorithmIdentifier, key: CryptoKey, data: ArrayBuffer) => Promise<ArrayBuffer>; unwrapKey: (format: "raw" | "spki" | "pkcs8" | "jwk", wrappedKey: ArrayBuffer, unwrappingKey: CryptoKey, unwrapAlgorithm: AlgorithmIdentifier, unwrappedKeyAlgorithm: AlgorithmIdentifier, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey>; verify: (algorithm: AlgorithmIdentifier, key: CryptoKey, signature: ArrayBuffer, data: ArrayBuffer) => Promise<boolean>; wrapKey: (format: "raw" | "spki" | "pkcs8" | "jwk", key: CryptoKey, wrappingKey: CryptoKey, wrapAlgorithm: AlgorithmIdentifier) => Promise<ArrayBuffer> }
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#subtle.description -->

The app's Web Crypto `SubtleCrypto` object, backed by the Roku runtime's crypto support.

It supports `digest`, HMAC, RSA, ECDSA and Ed25519 signing, RSA, ECDSA and Ed25519
verification, and `encrypt` and `decrypt` with the `DeviceCrypto` algorithm. Every other method,
and any unsupported algorithm, returns a promise that rejects with a not-implemented error.
