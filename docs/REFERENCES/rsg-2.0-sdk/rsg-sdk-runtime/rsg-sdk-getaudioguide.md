---
title: 'getAudioGuide'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getAudioGuide'
  description: 'Returns the runtime''s Audio Guide, which speaks text through the device''s screen reader.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getcomponentlibraryfactory
      title: 'getComponentLibraryFactory'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/audio-guide.ts#getAudioGuide.deck -->

Returns the runtime's Audio Guide, which speaks text through the device's screen reader

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/audio-guide.ts`. -->

```typescript
import { getAudioGuide } from "@roku-sdk/runtime/audio-guide";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/audio-guide.ts#getAudioGuide.signature -->

```typescript
getAudioGuide(): AudioGuide
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/audio-guide.ts#getAudioGuide.description -->

Returns the runtime's Audio Guide, which speaks text through the device's screen reader.

Use it to announce app content to users who have Audio Guide turned on, for CVAA accessibility.
For general-purpose speech that is not tied to the screen reader, use [getTextToSpeech](doc:rsg-sdk-gettexttospeech).
The object is created on the first call and reused afterwards.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/audio-guide.ts#getAudioGuide.returns -->

The runtime's `AudioGuide` object.
