# ScheduledMessageListResponse

Messages list

## Example Usage

```typescript
import { ScheduledMessageListResponse } from "bereach/models/operations";

let value: ScheduledMessageListResponse = {
  success: true,
  messages: [
    {
      id: "<id>",
      contactId: "<id>",
      message: "<value>",
      status: "scheduled",
      sentAt: "<value>",
      campaignSlug: "<value>",
      createdAt: "1708749500337",
    },
  ],
  total: 876464,
  limit: 149047,
  offset: 282829,
  creditsUsed: 685127,
  retryAfter: 801151,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `messages`                                                                                                                           | [operations.ScheduledMessageListMessage](../../models/operations/scheduled-message-list-message.md)[]                                | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `total`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `limit`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `offset`                                                                                                                             | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ScheduledMessageListSpent](../../models/operations/scheduled-message-list-spent.md)                                      | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |