# CollectEngagersTotals

The post's own engagement badges and how much of them this run has read, summed across the posts read. A sum, so it can never answer how many came from one post: `perPost` answers that. Absent while `count` is above 0 means the badge could not be read, never that nobody engaged. Both zero or absent WITH count 0 is the only shape that means no visible engagement on this page.

## Example Usage

```typescript
import { CollectEngagersTotals } from "bereach/models/operations";

let value: CollectEngagersTotals = {};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `likes`                                                                              | *number*                                                                             | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `comments`                                                                           | *number*                                                                             | :heavy_minus_sign:                                                                   | Top-level comments on the post. The number shown on a post adds the replies to this. |
| `likesRead`                                                                          | *number*                                                                             | :heavy_minus_sign:                                                                   | Reactions read so far, in the same unit as `likes`.                                  |
| `commentsRead`                                                                       | *number*                                                                             | :heavy_minus_sign:                                                                   | Top-level comments read so far, in the same unit as `comments`.                      |
| `replies`                                                                            | *number*                                                                             | :heavy_minus_sign:                                                                   | Replies under the comments read so far.                                              |
| `commentsShown`                                                                      | *number*                                                                             | :heavy_minus_sign:                                                                   | The comment number shown on the post, comments and replies together.                 |