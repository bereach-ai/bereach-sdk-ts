# GetOwnPostsResponse

The user's own posts

## Example Usage

```typescript
import { GetOwnPostsResponse } from "bereach/models/operations";

let value: GetOwnPostsResponse = {
  success: true,
  posts: [],
  count: 341035,
  total: 698266,
  start: 668015,
  hasMore: true,
  paginationToken: "<value>",
  creditsUsed: 660806,
  retryAfter: 475448,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `posts`                                                                                                                              | [operations.GetOwnPostsPost](../../models/operations/get-own-posts-post.md)[]                                                        | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `count`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Posts in THIS page.                                                                                                                  |
| `total`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Posts LinkedIn reports in total.                                                                                                     |
| `start`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Offset this page started at.                                                                                                         |
| `hasMore`                                                                                                                            | *boolean*                                                                                                                            | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `paginationToken`                                                                                                                    | *string*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Cursor for the next page, or null on the last one.                                                                                   |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.GetOwnPostsSpent](../../models/operations/get-own-posts-spent.md)                                                        | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |