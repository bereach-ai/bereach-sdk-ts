# SearchJobsResponse

List of LinkedIn job listings matching the search criteria

## Example Usage

```typescript
import { SearchJobsResponse } from "bereach/models/operations";

let value: SearchJobsResponse = {
  success: true,
  category: "jobs",
  items: [],
  paging: {
    start: 968233,
    count: 443508,
    total: 906771,
  },
  hasMore: false,
  creditsUsed: 595366,
  retryAfter: 173084,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `category`                                                                                                                           | [operations.SearchJobsCategory](../../models/operations/search-jobs-category.md)                                                     | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `items`                                                                                                                              | [operations.SearchJobsItem](../../models/operations/search-jobs-item.md)[]                                                           | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `paging`                                                                                                                             | [operations.SearchJobsPaging](../../models/operations/search-jobs-paging.md)                                                         | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `hasMore`                                                                                                                            | *boolean*                                                                                                                            | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `warnings`                                                                                                                           | [operations.SearchJobsWarning](../../models/operations/search-jobs-warning.md)[]                                                     | :heavy_minus_sign:                                                                                                                   | Caveats about this result set. Absent or empty means the search ran exactly as asked.                                                |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.SearchJobsSpent](../../models/operations/search-jobs-spent.md)                                                           | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |