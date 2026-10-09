---
title: 'createSubtleCrypto'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'createSubtleCrypto'
  description: 'Creates a minimal SubtleCrypto implementation backed by Roku runtime crypto hosts.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-crypto
      title: 'crypto'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#createSubtleCrypto.deck -->

Creates a minimal SubtleCrypto implementation backed by Roku runtime crypto hosts

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/crypto.ts`. -->

```typescript
import { createSubtleCrypto } from "@roku-sdk/runtime/crypto";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/crypto.ts#createSubtleCrypto.signature -->

```typescript
createSubtleCrypto(): { decrypt: (algorithm: AlgorithmIdentifier, key: CryptoKey, data: ArrayBuffer) => Promise<ArrayBuffer>; deriveBits: (algorithm: AlgorithmIdentifier, baseKey: CryptoKey, length: number) => Promise<ArrayBuffer>; deriveKey: (algorithm: AlgorithmIdentifier, baseKey: CryptoKey, derivedKeyType: AlgorithmIdentifier | AesKeyGenParams | HmacKeyGenParams, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey>; digest: (algorithm: AlgorithmIdentifier, data: ArrayBuffer) => Promise<ArrayBuffer>; encrypt: (algorithm: AlgorithmIdentifier, key: CryptoKey, data: ArrayBuffer) => Promise<ArrayBuffer>; exportKey: (format: "raw" | "spki" | "pkcs8" | "jwk", key: CryptoKey) => Promise<ArrayBuffer | JsonWebKey>; generateKey: (algorithm: AlgorithmIdentifier, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey | CryptoKeyPair>; importKey: (format: "raw" | "spki" | "pkcs8" | "jwk", keyData: ArrayBuffer | JsonWebKey, algorithm: AlgorithmIdentifier, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey>; sign: (algorithm: AlgorithmIdentifier, key: CryptoKey, data: ArrayBuffer) => Promise<ArrayBuffer>; unwrapKey: (format: "raw" | "spki" | "pkcs8" | "jwk", wrappedKey: ArrayBuffer, unwrappingKey: CryptoKey, unwrapAlgorithm: AlgorithmIdentifier, unwrappedKeyAlgorithm: AlgorithmIdentifier, extractable: boolean, keyUsages: KeyUsage[]) => Promise<CryptoKey>; verify: (algorithm: AlgorithmIdentifier, key: CryptoKey, signature: ArrayBuffer, data: ArrayBuffer) => Promise<boolean>; wrapKey: (format: "raw" | "spki" | "pkcs8" | "jwk", key: CryptoKey, wrappingKey: CryptoKey, wrapAlgorithm: AlgorithmIdentifier) => Promise<ArrayBuffer> }
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#createSubtleCrypto.description -->

Creates a minimal SubtleCrypto implementation backed by Roku runtime crypto hosts.

Supported operations include DeviceCrypto encryption/decryption, HMAC/RSA/ECDSA/Ed25519 signing
and verification, and digest computation.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/crypto.ts#createSubtleCrypto.returns -->

An object implementing the supported SubtleCrypto methods.
