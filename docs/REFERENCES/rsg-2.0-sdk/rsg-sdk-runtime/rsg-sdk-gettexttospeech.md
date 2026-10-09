---
title: 'getTextToSpeech'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getTextToSpeech'
  description: 'Returns the runtime''s text-to-speech API, for speaking text whether or not the screen reader is on.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getvoicedictation
      title: 'getVoiceDictation'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/text-to-speech.ts#getTextToSpeech.deck -->

Returns the runtime's text-to-speech API, for speaking text whether or not the screen reader is on

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/text-to-speech.ts`. -->

```typescript
import { getTextToSpeech } from "@roku-sdk/runtime/text-to-speech";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/text-to-speech.ts#getTextToSpeech.signature -->

```typescript
getTextToSpeech(): TextToSpeech
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/text-to-speech.ts#getTextToSpeech.description -->

Returns the runtime's text-to-speech API, for speaking text whether or not the screen reader is
on.

Use it for speech that is part of the app's own behavior, and control the rate, pitch and volume
on the returned object. To announce content for the screen reader, use [getAudioGuide](doc:rsg-sdk-getaudioguide)
instead. The object is created on the first call and reused afterwards.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/text-to-speech.ts#getTextToSpeech.returns -->

The runtime's `TextToSpeech` object.
