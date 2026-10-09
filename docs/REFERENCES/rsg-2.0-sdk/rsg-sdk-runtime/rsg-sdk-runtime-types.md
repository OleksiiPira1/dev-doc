---
title: 'Runtime types'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'Runtime types'
  description: 'Types shared by several @roku-sdk/runtime exports, or used by none of them directly. Each is documented here once and linked from every page that uses it.'
  robots: index
next:
  description: ''
---

<!-- derived: rsg-sdk/external/packages/runtime/package.json#runtime-types.deck -->

Types shared by several `@roku-sdk/runtime` exports, or used by none of them directly

<!-- ⚠️ This page is generated — edit the JSDoc of each type in `rsg-sdk/external/packages/runtime/src`. -->

```typescript
import type {
    DeviceInfoEventsHook,
} from "@roku-sdk/runtime/device-info-events";
import type { InputEventsHook } from "@roku-sdk/runtime/input";
import type { LifecycleEventsHook } from "@roku-sdk/runtime/lifecycle";
```

<!-- derived: rsg-sdk/external/packages/runtime/package.json#runtime-types.intro -->

Each is documented here once and linked from every page that uses it.

## Types
<!-- generator-heading -->

### DeviceInfoEventsHook
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/device-info-events.ts#DeviceInfoEventsHook.description -->

An object of accessors for device-level events: the UI resolution, screensaver exit, network
link status, low-memory warnings and internet connectivity.

Each accessor is `null` until its first event. The hooks do not return this type: to subscribe
to these events, use [useUiResolution](doc:rsg-sdk-device-info) for the resolution and [useDeviceInfoEvents](doc:rsg-sdk-device-info)
for the others, which reports screensaver exits, link changes and internet changes as counters.

<!-- derived: rsg-sdk/external/packages/runtime/src/device-info-events.ts#DeviceInfoEventsHook.table -->

```typescript
type DeviceInfoEventsHook = unknown;
```

### InputEventsHook
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/input.ts#InputEventsHook.description -->

Return type for the `useInput` hook.

Provides reactive access to input events from the Roku runtime.
Both properties are SolidJS Accessors that update when input events occur.

<!-- derived: rsg-sdk/external/packages/runtime/src/input.ts#InputEventsHook.table -->

```typescript
type InputEventsHook = unknown;
```

### LifecycleEventsHook
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/lifecycle.ts#LifecycleEventsHook.description -->

Return type for the `useLifecycle` hook.

Provides reactive access to app lifecycle events (suspend/resume) from the Roku runtime.
Both properties are SolidJS Accessors that update when lifecycle events occur.

<!-- derived: rsg-sdk/external/packages/runtime/src/lifecycle.ts#LifecycleEventsHook.table -->

```typescript
type LifecycleEventsHook = unknown;
```
