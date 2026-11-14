# ContextSetResponseBody1

## Example Usage

```typescript
import { ContextSetResponseBody1 } from "bereach/models/operations";

let value: ContextSetResponseBody1 = {
  success: true,
  entry: {
    id: "<id>",
    type: "<value>",
    label: "<value>",
    content: "<value>",
    scope: "<value>",
    updatedAt: "1735627605473",
  },
  creditsUsed: 443677,
  retryAfter: 264509,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `entry`                                                                                                                              | [operations.ContextSetEntry](../../models/operations/context-set-entry.md)                                                           | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContextSetSpent1](../../models/operations/context-set-spent1.md)                                                         | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |