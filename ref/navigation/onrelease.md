---
title: 'onRelease'
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: 'onRelease'
  description: 'Wraps a handler so it fires only on key-up (release).'
  robots: index
next:
  description: ''
---

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#onRelease.deck -->

Wraps a handler so it fires only on key-up (release)

> ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx`.

```typescript
import { onRelease } from "@roku-sdk/navigation";
```

**Package:** `@roku-sdk/navigation`

### onRelease
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#onRelease.signature -->

```typescript
onRelease(handler: () => KeyResult): KeyPressHandler
```

#### Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#onRelease.description -->

Wraps a handler so it fires only on key-up (release). Mirrors [onPress](onpress.md): the handler's
verdict is passed through on the release, and the press consumes.

#### Parameters
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#onRelease.params -->

| Name | Type | Description |
| --- | --- | --- |
| `handler` | `() => KeyResult` |  |

#### Return values
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#onRelease.returns -->

Returns `KeyPressHandler`.

#### Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#onRelease.example -->

```ts
onKey: { play: onRelease(() => stop()) }
// equivalent to: play: press => { if (!press) stop(); }
```
