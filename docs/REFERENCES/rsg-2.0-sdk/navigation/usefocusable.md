---
title: 'useFocusable'
excerpt: 'Registers a component instance with the nearest FocusBoundary'
deprecated: false
hidden: true
metadata:
  title: 'useFocusable'
  description: 'Registers a component instance with the nearest FocusBoundary.'
  robots: index
next:
  description: ''
---

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#useFocusable.deck -->

Registers a component instance with the nearest `FocusBoundary`

> ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx`.

```typescript
import { useFocusable } from "@roku-sdk/navigation";
```

**Package:** `@roku-sdk/navigation`

### useFocusable

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#useFocusable.signature -->

```typescript
useFocusable(options: UseFocusableOptions): { focus: () => void; focusId: object; hasFootprint: () => boolean; isFocused: () => boolean; ref: (el: unknown) => void }
```

#### Description

<!-- src: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#useFocusable.description -->

Registers a component instance with the nearest `FocusBoundary`.

Must be called inside a component rendered within a `RootFocusBoundary` or `FocusBoundary`.
Registration (and the ordering of focusables for navigation) follows render order.

#### Parameters

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#useFocusable.params -->

| Name | Type | Description |
| --- | --- | --- |
| `options` | [UseFocusableOptions](doc:usefocusable#usefocusableoptions) | Options passed to `useFocusable`. Extends `FocusHandlers` with an optional pre-created `focusId` identity. |

#### Return values

<!-- src: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#useFocusable.returns -->

- `ref` — ref callback to attach to the root JSX element. Always defined — captures
   the DomNode for `RootFocusBoundary` focus-path computation (no-op when the root
   boundary has no `setFocusPath`).
- `focusId` — the stable identity object used by the focus system. Only needed when
   you let `useFocusable` auto-create the identity and need to pass it elsewhere
   programmatically. When you pre-create the identity via `options.focusId`, you already
   have it — `focusId` just mirrors it back.
- `isFocused()` — reactive accessor; use to drive visual focus state
- `hasFootprint()` — reactive accessor; `true` when this item is the remembered focus
   target but the boundary is inactive (SG focus is elsewhere). Use to render a dimmed
   focus indicator so the user knows where focus will land on return.
- `focus()` — imperatively move virtual focus to this component

#### Example

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#useFocusable.example -->

```tsx
const { isFocused, ref } = useFocusable({
    focusId: props.focusId,
    onKey: {
        [RemoteKey.Select]: press => {
            if (press) props.onSelect?.();
        }
    }
} satisfies UseFocusableOptions);

return (
    <group ref={ref} translation={[0, props.y]}>
        <rectangle width={400} height={56} color={isFocused() ? "0x0055DDFF" : "0x222222FF"} />
        <label text={props.label} color={isFocused() ? "0xFFFFFFFF" : "0xBBBBBBFF"} translation={[16, 14]} />
    </group>
);
```

## Types

### UseFocusableOptions

<!-- src: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#UseFocusableOptions.description -->

Options passed to `useFocusable`.
Extends `FocusHandlers` with an optional pre-created `focusId` identity.

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#UseFocusableOptions.table -->

| Name | Type | Description |
| --- | --- | --- |
| `focusId?` | `FocusId` | A pre-created stable object to use as this component's virtual focus identity. Use this when you need to pass the identity to `FocusBoundary`'s `initialFocus` prop.  If omitted, `useFocusable` creates a new `{}` object automatically. |

Extends [FocusHandlers](doc:usefocusable#focushandlers).

### FocusHandlers

<!-- src: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#FocusHandlers.description -->

Handler interface that a focusable component can provide when calling `useFocusable`.
All fields are optional.

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-boundary.tsx#FocusHandlers.table -->

| Name | Type | Description |
| --- | --- | --- |
| `canReceiveFocus?` | `() => boolean` | If provided, the boundary will only move virtual focus here when this returns `true`. Defaults to always focusable. |
| `onFocusGained?` | `() => void` | Called when this component gains virtual focus. |
| `onFocusLost?` | `() => void` | Called when this component loses virtual focus. |
| `onKey?` | `KeyHandlerMap` | Declarative key handler map. Each key in the record is a remote key name that this component handles. The boundary derives `handledKeys` from `Object.keys(onKey)` and evaluates any `when` gates reactively.  Dispatch: when a key event arrives and the key exists in `onKey`, the handler is called directly. If the entry has a `when` gate that returns `false` at dispatch time, the handler is skipped and the key is treated as unhandled. |
