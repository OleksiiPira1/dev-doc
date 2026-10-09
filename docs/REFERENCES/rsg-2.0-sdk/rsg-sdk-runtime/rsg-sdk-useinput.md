---
title: 'useInput'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'useInput'
  description: 'Hook for accessing input events from the Roku runtime.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-uselaunchconfig
      title: 'useLaunchConfig'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/input.ts#useInput.deck -->

Hook for accessing input events from the Roku runtime

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/input.ts`. -->

```typescript
import { useInput } from "@roku-sdk/runtime/input";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/input.ts#useInput.signature -->

```typescript
const useInput: () => { inputParams: Accessor<InputParams | null>; voiceInputParams: Accessor<VoiceInputParams | null> } & { updateVoiceInputStatus: (params: { id: number; status: VoiceHandledStatus }) => boolean }
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/input.ts#useInput.description -->

Hook for accessing input events from the Roku runtime.

Provides reactive access to both standard input events and voice input events.
The hook automatically sets up input handlers when the component mounts and
cleans them up when it unmounts.

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/input.ts#useInput.example -->

```ts
// Basic usage
const input = useInput();

createEffect(() => {
    const params = input.inputParams();
    if (params) {
        console.log('Input received:', JSON.stringify(params));
    }
});
```

```ts
// Listen to voice input
const input = useInput();

createEffect(() => {
    const voiceParams = input.voiceInputParams();
    if (voiceParams) {
        console.log('Voice transcription:', JSON.stringify(voiceParams));
    }
});
```
