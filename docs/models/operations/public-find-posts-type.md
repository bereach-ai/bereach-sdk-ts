# PublicFindPostsType

What the post carries: 'image' (one picture or several), 'video', 'document' (what the feed shows as a carousel of pages, usually a PDF), or 'article' (a link to an article or newsletter).

## Example Usage

```typescript
import { PublicFindPostsType } from "bereach/models/operations";

let value: PublicFindPostsType = "document";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"image" | "video" | "document" | "article" | Unrecognized<string>
```