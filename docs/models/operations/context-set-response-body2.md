# ContextSetResponseBody2

## Example Usage

```typescript
import { ContextSetResponseBody2 } from "bereach/models/operations";

let value: ContextSetResponseBody2 = {
  success: true,
  removed: {
    type: "<value>",
    label: null,
    scope: "<value>",
  },
  unboundFrom: [],
  creditsUsed: 824563,
  retryAfter: 100745,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `removed`                                                                                                                            | [operations.Removed](../../models/operations/removed.md)                                                                             | :heavy_check_mark:                                                                                                                   | The memory that was deleted.                                                                                                         |
| `unboundFrom`                                                                                                                        | *string*[]                                                                                                                           | :heavy_check_mark:                                                                                                                   | Names of the lists that used it and no longer do.                                                                                    |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContextSetSpent2](../../models/operations/context-set-spent2.md)                                                         | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |