# SearchPostsResponse

Public posts matching the search

## Example Usage

```typescript
import { SearchPostsResponse } from "bereach/models/operations";

let value: SearchPostsResponse = {
  success: true,
  category: "posts",
  items: [
    {
      postUrl: "https://upset-cook.com",
      text: "<value>",
      date: 331248,
      likesCount: 277560,
      commentsCount: 56909,
      sharesCount: 384396,
      postUrn: "<value>",
      postId: "<id>",
      type: "POST",
      author: {
        name: "<value>",
        profileUrl: "https://criminal-forager.net",
        headline: "<value>",
        profilePicture: "<value>",
        isCompany: false,
        publicIdentifier: "<value>",
        profileUrn: "<value>",
      },
      isRepost: true,
    },
  ],
  count: 498291,
  paging: {
    start: 122536,
    count: 91169,
    total: 569226,
  },
  hasMore: true,
  creditsUsed: 634230,
  retryAfter: 112477,
};
```

## Fields

| Field                                                                                                                                                             | Type                                                                                                                                                              | Required                                                                                                                                                          | Description                                                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                                         | *true*                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                | N/A                                                                                                                                                               |
| `category`                                                                                                                                                        | [operations.SearchPostsCategory](../../models/operations/search-posts-category.md)                                                                                | :heavy_check_mark:                                                                                                                                                | N/A                                                                                                                                                               |
| `items`                                                                                                                                                           | [operations.SearchPostsItem](../../models/operations/search-posts-item.md)[]                                                                                      | :heavy_check_mark:                                                                                                                                                | N/A                                                                                                                                                               |
| `count`                                                                                                                                                           | *number*                                                                                                                                                          | :heavy_check_mark:                                                                                                                                                | How many items this page returned.                                                                                                                                |
| `saved`                                                                                                                                                           | *number*                                                                                                                                                          | :heavy_minus_sign:                                                                                                                                                | People from this page written to the contact list. Null or absent means the write has not answered: report nothing saved rather than the number of rows returned. |
| `paging`                                                                                                                                                          | [operations.SearchPostsPaging](../../models/operations/search-posts-paging.md)                                                                                    | :heavy_check_mark:                                                                                                                                                | N/A                                                                                                                                                               |
| `hasMore`                                                                                                                                                         | *boolean*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                                | True when a call with `start` past 0 can return more posts.                                                                                                       |
| `warnings`                                                                                                                                                        | [operations.SearchPostsWarning](../../models/operations/search-posts-warning.md)[]                                                                                | :heavy_minus_sign:                                                                                                                                                | Caveats about this result set. NOT_SEARCHED: a field of the request this search did not apply. Absent or empty means the search ran exactly as asked.             |
| `ignoredFields`                                                                                                                                                   | [operations.SearchPostsIgnoredField](../../models/operations/search-posts-ignored-field.md)[]                                                                     | :heavy_minus_sign:                                                                                                                                                | Fields of the request this search did not apply, each also explained by a NOT_SEARCHED warning. Absent when every field was applied.                              |
| `note`                                                                                                                                                            | *string*                                                                                                                                                          | :heavy_minus_sign:                                                                                                                                                | One sentence about this answer a person can read, such as why it is empty.                                                                                        |
| `creditsUsed`                                                                                                                                                     | *number*                                                                                                                                                          | :heavy_check_mark:                                                                                                                                                | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged.                              |
| `spent`                                                                                                                                                           | [operations.SearchPostsSpent](../../models/operations/search-posts-spent.md)                                                                                      | :heavy_minus_sign:                                                                                                                                                | What this call spent, in money: the figure to tell the user, written as text says it.                                                                             |
| `retryAfter`                                                                                                                                                      | *number*                                                                                                                                                          | :heavy_check_mark:                                                                                                                                                | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                                                  |