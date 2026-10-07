---
title: '@roku-sdk/navigation'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: '@roku-sdk/navigation'
  description: 'Navigation primitives for Roku SDK applications.'
  robots: index
next:
  description: ''
---

<!-- derived: rsg-sdk/external/packages/navigation/README.md#navigation.deck -->

Navigation primitives for Roku SDK applications

> ⚠️ This page is generated — edit the package README in `rsg-sdk/external/packages/navigation/README.md` and the JSDoc of each export.

**Package:** `@roku-sdk/navigation`

<!-- derived: rsg-sdk/external/packages/navigation/README.md#navigation.intro -->

Navigation primitives for Roku SDK applications.

## Pages
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/navigation/README.md#navigation.pages -->

- [bubble](doc:bubble) — Return from a key handler to pass the key on instead of consuming it.
- [computeSGPath](doc:computesgpath) — Compute the SceneGraph tree index path from root to target by walking bottom-up using parent pointers.
- [FocusBoundary](doc:focusboundary) — Establishes a virtual focus boundary for a subtree of TypeScript components.
- [FocusPathCtx](doc:focuspathctx) — Context that RootFocusBoundary provides when its setFocusPath prop is set, so that useFocusable can report which SceneGraph node holds virtual focus.
- [ModalBoundary](doc:modalboundary) — Renders a custom dialog with its own FocusBoundary, dismissed by the Back key.
- [onPress](doc:onpress) — Wraps a handler so it fires only on key-down (press), removing the need for an if (press) guard inside onKey (or onUnhandledKey) handlers.
- [onRelease](doc:onrelease) — Wraps a handler so it fires only on key-up (release).
- [RootFocusBoundary](doc:rootfocusboundary) — The root of a virtual focus tree for a single anchor node.
- [ScreenControllerContext](doc:screencontrollercontext) — Context for managing the screen stack provided by ScreenControllerProvider.
- [ScreenControllerProvider](doc:screencontrollerprovider) — Provider for ScreenControllerContext.
- [useFocusable](doc:usefocusable) — Registers a component instance with the nearest FocusBoundary.
- [useFocusActions](doc:usefocusactions) — Returns imperative focus actions for the nearest FocusBoundary.
- [useModal](doc:usemodal) — Creates modal open/close state and focus-transfer actions.
- [Navigation types](doc:navigation-types) — Types shared by several `@roku-sdk/navigation` exports.
