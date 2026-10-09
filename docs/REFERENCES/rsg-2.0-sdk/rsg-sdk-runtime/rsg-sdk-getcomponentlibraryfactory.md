---
title: 'getComponentLibraryFactory'
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: 'getComponentLibraryFactory'
  description: 'Resolves to the runtime''s component library factory, which creates dynamic component libraries (DCLs) for a TypeScript app.'
  robots: index
next:
  description: ''
  pages:
    - slug: rsg-sdk-getfilesystem
      title: 'getFileSystem'
      type: basic
---

<!-- derived: rsg-sdk/external/packages/runtime/src/component-library.ts#getComponentLibraryFactory.deck -->

Resolves to the runtime's component library factory, which creates dynamic component libraries (DCLs) for a TypeScript app

<!-- ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/runtime/src/component-library.ts`. -->

```typescript
import {
    getComponentLibraryFactory,
} from "@roku-sdk/runtime/component-library";
```

<!-- derived: rsg-sdk/external/packages/runtime/src/component-library.ts#getComponentLibraryFactory.signature -->

```typescript
const getComponentLibraryFactory: () => Promise<ComponentLibraryFactory>
```

## Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/runtime/src/component-library.ts#getComponentLibraryFactory.description -->

Resolves to the runtime's component library factory, which creates dynamic component libraries
(DCLs) for a TypeScript app.

Call `createLibrary(name)` on the result with the name of a DCL that the app declares, then
load it and watch its load status on the returned `ComponentLibrary`.
`createLibrary` throws if the name is invalid or the library cannot be created.
