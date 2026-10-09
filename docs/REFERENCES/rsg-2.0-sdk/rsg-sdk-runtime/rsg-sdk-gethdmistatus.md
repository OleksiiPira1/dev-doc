---
title: 'getHdmiStatus'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getHdmiStatus'
  description: 'Get the HdmiStatus runtime API with query methods only.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getperfetto
      title: 'getPerfetto'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/hdmi-status.ts#getHdmiStatus.deck -->

Get the HdmiStatus runtime API with query methods only

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/hdmi-status.ts`. -->

```typescript
import { getHdmiStatus } from "@roku-sdk/runtime/hdmi-status";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/hdmi-status.ts#getHdmiStatus.signature -->

```typescript
getHdmiStatus(): Promise<HdmiStatus | null>
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/hdmi-status.ts#getHdmiStatus.description -->

Get the HdmiStatus runtime API with query methods only.

For reactive HDMI hot-plug and ALLM events, use [useHdmiStatus](doc:rsg-sdk-usehdmistatus).

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/hdmi-status.ts#getHdmiStatus.returns -->

Promise resolved with the safe HdmiStatus wrapper, or `null` when unavailable.

## Types
<!-- generator-heading -->

### HdmiStatus
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/hdmi-status.ts#HdmiStatus.description -->

Safe query surface exposed to app code (event handlers belong in [useHdmiStatus](doc:rsg-sdk-usehdmistatus)).

<!-- derived: rsg-sdk/external/packages/runtime/src/hdmi-status.ts#HdmiStatus.table -->

```typescript
type HdmiStatus = unknown;
```
