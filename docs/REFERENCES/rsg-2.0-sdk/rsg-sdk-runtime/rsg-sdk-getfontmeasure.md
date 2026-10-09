---
title: 'getFontMeasure'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getFontMeasure'
  description: 'Returns the runtime''s font measurement API, for measuring how text will render in a given font.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-gethdmistatus
      title: 'getHdmiStatus'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/font.ts#getFontMeasure.deck -->

Returns the runtime's font measurement API, for measuring how text will render in a given font

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/font.ts`. -->

```typescript
import { getFontMeasure } from "@roku-sdk/runtime/font";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/font.ts#getFontMeasure.signature -->

```typescript
const getFontMeasure: () => FontMeasureApi
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/font.ts#getFontMeasure.description -->

Returns the runtime's font measurement API, for measuring how text will render in a given font.

Use it to size or lay out labels from text metrics such as a line's width and height or the
font's ascent and descent, all in pixels. The call is synchronous, and the runtime object is
fetched on the first call and reused afterwards.
