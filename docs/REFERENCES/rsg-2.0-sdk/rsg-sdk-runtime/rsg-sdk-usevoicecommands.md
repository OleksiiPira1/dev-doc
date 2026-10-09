---
title: 'useVoiceCommands'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'useVoiceCommands'
  description: 'Hook for reactive non-dictation voice commands (play, pause, seek, etc.).'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-usevoicedictation
      title: 'useVoiceDictation'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/voice-commands.ts#useVoiceCommands.deck -->

Hook for reactive non-dictation voice commands (`play`, `pause`, `seek`, etc.)

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/voice-commands.ts`. -->

```typescript
import { useVoiceCommands } from "@roku-sdk/runtime/voice-commands";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/voice-commands.ts#useVoiceCommands.signature -->

```typescript
useVoiceCommands(): VoiceCommandHook
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/voice-commands.ts#useVoiceCommands.description -->

Hook for reactive non-dictation voice commands (`play`, `pause`, `seek`, etc.).

Firmware routes media and navigation voice commands through the voice input
handler. This hook hides that wiring: it subscribes to [useInput](doc:rsg-sdk-useinput)
internally and exposes a single `commandParams` signal filtered to events
whose `command` is not `"dictation"`.

Unlike [useVoiceDictation](doc:rsg-sdk-usevoicedictation), this hook does **not** auto-acknowledge
events. The app must call `respond(status)` with an appropriate
`VoiceHandledStatus` once it has handled (or declined) the command.
Firmware blocks up to 5s per event until the app responds.

Because the ack is the app's job, `commandParams` is published synchronously
as each event arrives: consumers run — and get a chance to `respond` — before
the next command can overwrite the signal. Deferring the publish would let two
commands arriving back to back collapse into one, leaving the first
unanswered until firmware times it out.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/voice-commands.ts#useVoiceCommands.returns -->

[VoiceCommandHook](doc:rsg-sdk-usevoicecommands#voicecommandhook) with a reactive `commandParams` accessor
and a `respond` method to acknowledge the latest command.

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/voice-commands.ts#useVoiceCommands.example -->

```ts
const { commandParams, respond } = useVoiceCommands();

createEffect(() => {
    const params = commandParams();
    if (!params) return;
    switch (params.command) {
        case "play":
            startPlayback();
            respond("success");
            break;
        case "pause":
            pausePlayback();
            respond("success");
            break;
        default:
            respond("unhandled");
    }
});
```

## Types
<!-- generator-heading -->

### VoiceCommandHook
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/voice-commands.ts#VoiceCommandHook.description -->

Return type for the [useVoiceCommands](doc:rsg-sdk-usevoicecommands) hook.

<!-- derived: rsg-sdk/external/packages/runtime/src/voice-commands.ts#VoiceCommandHook.table -->

```typescript
type VoiceCommandHook = unknown;
```
