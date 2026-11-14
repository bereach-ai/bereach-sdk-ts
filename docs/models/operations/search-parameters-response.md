# SearchParametersResponse

Matching ids, or a hint explaining why there were none

## Example Usage

```typescript
import { SearchParametersResponse } from "bereach/models/operations";

let value: SearchParametersResponse = {
  success: true,
  items: [
    {
      id: "<id>",
      title: "<value>",
      type: "<value>",
    },
  ],
  count: 217655,
  aliasResolved: true,
  creditsUsed: 352637,
  retryAfter: 211549,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `items`                                                                                                                              | [operations.SearchParametersItem](../../models/operations/search-parameters-item.md)[]                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `count`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `hint`                                                                                                                               | *string*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | Present ONLY when nothing matched, and it says why rather than leaving an empty array to be read as an empty world.                  |
| `aliasResolved`                                                                                                                      | *boolean*                                                                                                                            | :heavy_check_mark:                                                                                                                   | True when the curated alias map answered rather than LinkedIn.                                                                       |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.SearchParametersSpent](../../models/operations/search-parameters-spent.md)                                               | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |