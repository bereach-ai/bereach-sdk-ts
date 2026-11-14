# InboxUnreadCountResponse

Unread count

## Example Usage

```typescript
import { InboxUnreadCountResponse } from "bereach/models/operations";

let value: InboxUnreadCountResponse = {
  success: true,
  unreadCount: 606353,
  creditsUsed: 486794,
  retryAfter: 462335,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `unreadCount`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Number of unread conversations/messages                                                                                              |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.InboxUnreadCountSpent](../../models/operations/inbox-unread-count-spent.md)                                              | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |