# InboxMessagesResponse

Conversation messages

## Example Usage

```typescript
import { InboxMessagesResponse } from "bereach/models/operations";

let value: InboxMessagesResponse = {
  success: true,
  messages: [],
  prevCursor: 615925,
  creditsUsed: 376086,
  retryAfter: 88401,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `messages`                                                                                                                           | [operations.InboxMessagesMessage](../../models/operations/inbox-messages-message.md)[]                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `prevCursor`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | deliveredAt timestamp (ms) of the oldest message: pass as 'deliveredAt' to load older messages. Null when no more messages.          |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.InboxMessagesSpent](../../models/operations/inbox-messages-spent.md)                                                     | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |