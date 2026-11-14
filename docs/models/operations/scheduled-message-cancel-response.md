# ScheduledMessageCancelResponse

Messages cancelled

## Example Usage

```typescript
import { ScheduledMessageCancelResponse } from "bereach/models/operations";

let value: ScheduledMessageCancelResponse = {
  success: true,
  cancelled: 384538,
  creditsUsed: 765358,
  retryAfter: 28700,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `cancelled`                                                                                                                          | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `ineligible`                                                                                                                         | [operations.ScheduledMessageCancelIneligible](../../models/operations/scheduled-message-cancel-ineligible.md)[]                      | :heavy_minus_sign:                                                                                                                   | Named messages that could not be cancelled, with the status they were in.                                                            |
| `notFound`                                                                                                                           | *string*[]                                                                                                                           | :heavy_minus_sign:                                                                                                                   | Named message ids that match nothing.                                                                                                |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ScheduledMessageCancelSpent](../../models/operations/scheduled-message-cancel-spent.md)                                  | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |