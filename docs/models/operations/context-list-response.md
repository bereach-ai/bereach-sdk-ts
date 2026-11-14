# ContextListResponse

Context entries

## Example Usage

```typescript
import { ContextListResponse } from "bereach/models/operations";

let value: ContextListResponse = {
  success: true,
  entries: [],
  total: 65628,
  hasMore: false,
  offset: 126269,
  creditsUsed: 661447,
  retryAfter: 200835,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `entries`                                                                                                                            | [operations.ContextListEntry](../../models/operations/context-list-entry.md)[]                                                       | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `total`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Total matching entries                                                                                                               |
| `hasMore`                                                                                                                            | *boolean*                                                                                                                            | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `offset`                                                                                                                             | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Where this page started. Add the row count to it for the next page.                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContextListSpent](../../models/operations/context-list-spent.md)                                                         | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |