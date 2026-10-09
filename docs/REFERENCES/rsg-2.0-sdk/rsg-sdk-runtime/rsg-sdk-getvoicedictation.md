---
title: 'getVoiceDictation'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getVoiceDictation'
  description: 'Returns the roVoiceDictation runtime instance, used to control keyboard voice-entry sessions (start/stop listening, switch keyboard domain, report text-box…'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-randomuuid
      title: 'randomUUID'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/voice-dictation.ts#getVoiceDictation.deck -->

Returns the `roVoiceDictation` runtime instance, used to control keyboard voice-entry sessions (start/stop listening, switch keyboard domain, report text-box state)

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/voice-dictation.ts`. -->

```typescript
import { getVoiceDictation } from "@roku-sdk/runtime/voice-dictation";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/voice-dictation.ts#getVoiceDictation.signature -->

```typescript
getVoiceDictation(): VoiceDictation
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/voice-dictation.ts#getVoiceDictation.description -->

Returns the `roVoiceDictation` runtime instance, used to control keyboard
voice-entry sessions (start/stop listening, switch keyboard domain, report
text-box state).

The instance is cached after the first call. Recognized dictation text is
**not** returned by this API — subscribe to [useVoiceDictation](doc:rsg-sdk-usevoicedictation) to
receive dictation events (`start` / `text` / `end`) reactively.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/voice-dictation.ts#getVoiceDictation.returns -->

The cached `VoiceDictation` instance.

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/voice-dictation.ts#getVoiceDictation.example -->

```ts
const voiceDictation = getVoiceDictation();
const { dictationParams } = useVoiceDictation();

voiceDictation.setUseVoiceEntry(DictationKeyboardType.Generic);
voiceDictation.updateDictationParams("", 0, 200);
voiceDictation.pressedSoftMicButton();

createEffect(() => {
    const params = dictationParams();
    if (params?.dictation_event === DictationEvent.Text) {
        // ...append params.text...
    }
});

// ...user finishes...
voiceDictation.releasedSoftMicButton();
voiceDictation.clearVoiceEntry();
```
