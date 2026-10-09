---
title: 'getSignalBeacon'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getSignalBeacon'
  description: 'Returns the runtime''s signal beacon API, which reports app performance milestones to the device.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-gettexttospeech
      title: 'getTextToSpeech'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/signal-beacon.ts#getSignalBeacon.deck -->

Returns the runtime's signal beacon API, which reports app performance milestones to the device

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/signal-beacon.ts`. -->

```typescript
import { getSignalBeacon } from "@roku-sdk/runtime/signal-beacon";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/signal-beacon.ts#getSignalBeacon.signature -->

```typescript
const getSignalBeacon: () => SignalBeacon
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/signal-beacon.ts#getSignalBeacon.description -->

Returns the runtime's signal beacon API, which reports app performance milestones to the device.

Call `signal` with a beacon name to mark a milestone, for example `"AppLaunchComplete"` when the
app's first screen is ready, or `"AppDialogInitiate"` and `"AppDialogComplete"` around a dialog.
Roku uses these beacons to measure app launch and dialog times. The call is synchronous, and the
runtime object is fetched on the first call and reused afterwards.

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/signal-beacon.ts#getSignalBeacon.example -->

```ts
getSignalBeacon().signal("AppLaunchComplete");
```
