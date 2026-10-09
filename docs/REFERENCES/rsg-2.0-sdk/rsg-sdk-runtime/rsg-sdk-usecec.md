---
title: 'useCec'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'useCec'
  description: 'Returns a reactive accessor for the device''s HDMI-CEC active source status.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-usefilesystem
      title: 'useFileSystem'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/cec.ts#useCec.deck -->

Returns a reactive accessor for the device's HDMI-CEC active source status

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/cec.ts`. -->

```typescript
import { useCec } from "@roku-sdk/runtime/cec";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/cec.ts#useCec.signature -->

```typescript
const useCec: () => { cecStatus: Accessor<CecInfo | null> } & Record<string, never>
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/cec.ts#useCec.description -->

Returns a reactive accessor for the device's HDMI-CEC active source status.

CEC (Consumer Electronics Control) lets HDMI devices signal one another. `cecStatus` is `null`
until the runtime reports the first status, then holds the latest `CecInfo`: whether the device
is the active source on the HDMI input and, on firmware that reports it, the active source
state. Unrecognized state values from firmware are reported as `CecActiveSourceState.Unknown`.
If the CEC interface fails to initialize, the hook logs an error and `cecStatus` stays `null`.

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/cec.ts#useCec.example -->

```tsx
const { cecStatus } = useCec();
<label text={cecStatus()?.active ? "Active source" : "Not active"} />;
```
