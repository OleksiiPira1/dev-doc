---
title: 'useHdmiStatus'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'useHdmiStatus'
  description: 'Hook for reactive HDMI status and ALLM events from the Roku runtime.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-useinput
      title: 'useInput'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/hdmi-status.ts#useHdmiStatus.deck -->

Hook for reactive HDMI status and ALLM events from the Roku runtime

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/hdmi-status.ts`. -->

```typescript
import { useHdmiStatus } from "@roku-sdk/runtime/hdmi-status";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/hdmi-status.ts#useHdmiStatus.signature -->

```typescript
const useHdmiStatus: () => { allmStatus: Accessor<HdmiAllmStatusInfo | null>; status: Accessor<HdmiStatusInfo | null> } & Record<string, never>
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/hdmi-status.ts#useHdmiStatus.description -->

Hook for reactive HDMI status and ALLM events from the Roku runtime.
