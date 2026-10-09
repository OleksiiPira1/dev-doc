---
title: 'computeSGPath'
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: 'computeSGPath'
  description: 'Compute the SceneGraph tree index path from root to target by walking bottom-up using parent pointers.'
  robots: index
next:
  description: ''
---

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-path-provider.tsx#computeSGPath.deck -->

Compute the SceneGraph tree index path from `root` to `target` by walking bottom-up using parent pointers

> ⚠️ This page is generated — edit the source JSDoc in `rsg-sdk/external/packages/navigation/src/focus-boundary/focus-path-provider.tsx`.

```typescript
import { computeSGPath } from "@roku-sdk/navigation";
```

**Package:** `@roku-sdk/navigation`

### computeSGPath
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-path-provider.tsx#computeSGPath.signature -->

```typescript
computeSGPath(target: DomNode, root: DomNode): string
```

#### Description
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-path-provider.tsx#computeSGPath.description -->

Compute the SceneGraph tree index path from `root` to `target` by walking
bottom-up using parent pointers.

At each step, finds the node's index within its parent's `.c` array (which
mirrors the SG tree exactly), then moves up. Stops when it reaches `root`.

Cost: O(depth × average-sibling-count) — typically 5–15 steps with
`indexOf` on small child arrays. Much cheaper than top-down DFS for large
trees.

#### Parameters
<!-- generator-heading -->

<!-- derived: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-path-provider.tsx#computeSGPath.params -->

| Name | Type | Description |
| --- | --- | --- |
| `target` | `DomNode` |  |
| `root` | `DomNode` |  |

#### Return values
<!-- generator-heading -->

<!-- src: rsg-sdk/external/packages/navigation/src/focus-boundary/focus-path-provider.tsx#computeSGPath.returns -->

"/"-separated index string (e.g. `"0/1/0/3/0"`), or `""` if
         `target` is not a descendant of `root`.
