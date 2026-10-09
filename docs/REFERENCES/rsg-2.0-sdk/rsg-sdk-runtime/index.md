---
title: 'Runtime'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'Runtime'
  description: 'Getters and hooks that give a Roku SDK app access to Roku OS services such as device information, app lifecycle, remote input, the file system, voice…'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-createsubtlecrypto
      title: 'createSubtleCrypto'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/README.md#runtime.deck -->

Getters and hooks that give a Roku SDK app access to Roku OS services such as device information, app lifecycle, remote input, the file system, voice, accessibility and HDMI-CEC

<!-- ⚠️ This page is generated — edit the package README in `rsg-sdk/external/packages/runtime/README.md` and the JSDoc of each export. -->

## Pages
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/README.md#runtime.pages -->

- [createSubtleCrypto](doc:rsg-sdk-createsubtlecrypto): Creates a minimal SubtleCrypto implementation backed by Roku runtime crypto hosts.
- [crypto](doc:rsg-sdk-crypto): Runtime-compatible crypto shim exposing a subset of the Web Crypto API.
- [Device info](doc:rsg-sdk-device-info): Returns a snapshot of static device properties and dynamic methods.
- [getAppInfo](doc:rsg-sdk-getappinfo): Returns the app's metadata from the runtime, such as its ID, version, title and whether it is a sideloaded developer build.
- [getAppMemoryMonitor](doc:rsg-sdk-getappmemorymonitor): Resolves to an object for querying the app's memory usage and limits.
- [getAudioGuide](doc:rsg-sdk-getaudioguide): Returns the runtime's Audio Guide, which speaks text through the device's screen reader.
- [getComponentLibraryFactory](doc:rsg-sdk-getcomponentlibraryfactory): Resolves to the runtime's component library factory, which creates dynamic component libraries (DCLs) for a TypeScript app.
- [getFileSystem](doc:rsg-sdk-getfilesystem): Get a FileSystem API object exposing safe file operations.
- [getFontMeasure](doc:rsg-sdk-getfontmeasure): Returns the runtime's font measurement API, for measuring how text will render in a given font.
- [getHdmiStatus](doc:rsg-sdk-gethdmistatus): Get the HdmiStatus runtime API with query methods only.
- [getPerfetto](doc:rsg-sdk-getperfetto): Returns the runtime's Perfetto tracing API, for adding your own events to a performance trace.
- [getRandomBytes](doc:rsg-sdk-getrandombytes): Returns an ArrayBuffer containing length cryptographically secure random bytes.
- [getRandomValues](doc:rsg-sdk-getrandomvalues): Web Crypto-compatible getRandomValues: fills the provided typed array with cryptographically secure random bytes and returns it.
- [getRegistry](doc:rsg-sdk-getregistry): Resolves to the device registry, the app's persistent key-value storage.
- [getSignalBeacon](doc:rsg-sdk-getsignalbeacon): Returns the runtime's signal beacon API, which reports app performance milestones to the device.
- [getTextToSpeech](doc:rsg-sdk-gettexttospeech): Returns the runtime's text-to-speech API, for speaking text whether or not the screen reader is on.
- [getVoiceDictation](doc:rsg-sdk-getvoicedictation): Returns the roVoiceDictation runtime instance, used to control keyboard voice-entry sessions (start/stop listening, switch keyboard domain, report text-box state).
- [randomUUID](doc:rsg-sdk-randomuuid): Generates a version 4 UUID string using DeviceInfo.
- [subtle](doc:rsg-sdk-subtle): The app's Web Crypto SubtleCrypto object, backed by the Roku runtime's crypto support.
- [useAppMemoryMonitor](doc:rsg-sdk-useappmemorymonitor): Returns a reactive accessor for the memory warnings the runtime reports for the app.
- [useCec](doc:rsg-sdk-usecec): Returns a reactive accessor for the device's HDMI-CEC active source status.
- [useFileSystem](doc:rsg-sdk-usefilesystem): Hook for file system storage events for runtime signal-aware components.
- [useHdmiStatus](doc:rsg-sdk-usehdmistatus): Hook for reactive HDMI status and ALLM events from the Roku runtime.
- [useInput](doc:rsg-sdk-useinput): Hook for accessing input events from the Roku runtime.
- [useLaunchConfig](doc:rsg-sdk-uselaunchconfig): Returns a reactive accessor for the parameters the app was launched with.
- [useLifecycle](doc:rsg-sdk-uselifecycle): Hook for accessing app lifecycle events from the Roku runtime.
- [useVoiceCommands](doc:rsg-sdk-usevoicecommands): Hook for reactive non-dictation voice commands (play, pause, seek, etc.).
- [useVoiceDictation](doc:rsg-sdk-usevoicedictation): Hook for reactive roVoiceDictation events.
- [Runtime types](doc:rsg-sdk-runtime-types): Types shared by several `@roku-sdk/runtime` exports.
