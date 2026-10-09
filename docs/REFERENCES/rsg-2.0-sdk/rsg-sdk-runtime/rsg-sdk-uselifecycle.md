---
title: 'useLifecycle'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'useLifecycle'
  description: 'Hook for accessing app lifecycle events from the Roku runtime.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-usevoicecommands
      title: 'useVoiceCommands'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/lifecycle.ts#useLifecycle.deck -->

Hook for accessing app lifecycle events from the Roku runtime

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/lifecycle.ts`. -->

```typescript
import { useLifecycle } from "@roku-sdk/runtime/lifecycle";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/lifecycle.ts#useLifecycle.signature -->

```typescript
const useLifecycle: () => { resumeParams: Accessor<ResumeParams | null>; suspendParams: Accessor<SuspendParams | null> } & { completeResume: () => void; completeSuspend: () => void }
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/lifecycle.ts#useLifecycle.description -->

Hook for accessing app lifecycle events from the Roku runtime.

Provides reactive access to suspend and resume events that occur when:
- User exits the application (suspend)
- Screensaver appears (suspend)
- User relaunches the suspended app (resume)
- Deep link is triggered while app is suspended (resume with launch params)

The hook automatically sets up lifecycle handlers when the component mounts and
cleans them up when it unmounts.

**Important Notes:**
- You must call `completeSuspend()` within the suspend handler to signal completion
- If `completeSuspend()` is not called, the runtime will automatically freeze after 1 second
- You should call `completeResume()` after handling the resume event to make the UI visible
- Deep link launch parameters are included in the resume event

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/lifecycle.ts#useLifecycle.example -->

```ts
// Basic suspend handling
const lifecycle = useLifecycle();

createEffect(() => {
    const suspend = lifecycle.suspendParams();
    if (suspend) {
        console.log('Suspending:', suspend.lastSuspendOrResumeReason);
        // Save state, update UI
        lifecycle.completeSuspend();
    }
});
```

```ts
// Handle resume with deep links
const lifecycle = useLifecycle();

createEffect(() => {
    const resume = lifecycle.resumeParams();
    if (resume) {
        console.log('Resuming:', resume.lastSuspendOrResumeReason);

        // Check for deep link launch
        if (resume.launchParams.source === 'deeplink') {
            const contentId = resume.launchParams.contentId;
            navigateToContent(contentId);
        }

        // Signal completion to make UI visible
        lifecycle.completeResume();
    }
});
```

```ts
// Complete lifecycle management
const lifecycle = useLifecycle();

createEffect(() => {
    const suspend = lifecycle.suspendParams();
    if (suspend) {
        if (suspend.lastSuspendOrResumeReason === 'home') {
            console.log('User pressed Home button');
        } else if (suspend.lastSuspendOrResumeReason === 'screensaver') {
            console.log('Screensaver activated');
        }

        // Save app state
        saveApplicationState();

        // Must signal completion before 1s timeout
        lifecycle.completeSuspend();
    }
});

createEffect(() => {
    const resume = lifecycle.resumeParams();
    if (resume) {
        // Restore app state
        restoreApplicationState();

        // Handle launch parameters
        Object.entries(resume.launchParams).forEach(([key, value]) => {
            console.log(`Launch param ${key}: ${value}`);
        });

        lifecycle.completeResume();
    }
});
```
