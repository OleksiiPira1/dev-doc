---
title: 'useLaunchConfig'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'useLaunchConfig'
  description: 'Returns a reactive accessor for the parameters the app was launched with.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-uselifecycle
      title: 'useLifecycle'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/launch-config.ts#useLaunchConfig.deck -->

Returns a reactive accessor for the parameters the app was launched with

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/launch-config.ts`. -->

```typescript
import { useLaunchConfig } from "@roku-sdk/runtime/launch-config";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/launch-config.ts#useLaunchConfig.signature -->

```typescript
useLaunchConfig(): { launchParams: Accessor<T> }
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/launch-config.ts#useLaunchConfig.description -->

Returns a reactive accessor for the parameters the app was launched with.

`launchParams` holds the launch parameters as string key-value pairs, such as a deep link's
`contentId` and `mediaType`. It is an empty object until the runtime delivers the parameters,
and it updates when the runtime reports new ones. Pass a type argument to name the parameters
your app expects.

## Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/launch-config.ts#useLaunchConfig.returns -->

An object with a `launchParams` accessor.

## Example
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/runtime/src/launch-config.ts#useLaunchConfig.example -->

```tsx
const { launchParams } = useLaunchConfig<{ contentId: string; mediaType: string }>();
createEffect(() => console.log("Deep link:", launchParams().contentId));
```
