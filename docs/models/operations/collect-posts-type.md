# CollectPostsType

The kind of address in postUrn, NOT the post's format: posts read from public records are always addressed by their 'activity' id. Read the format from media.

## Example Usage

```typescript
import { CollectPostsType } from "bereach/models/operations";

let value: CollectPostsType = "ugcPost";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"activity" | "ugcPost" | "share" | Unrecognized<string>
```