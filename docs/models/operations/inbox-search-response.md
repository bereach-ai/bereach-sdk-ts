# InboxSearchResponse

Matching conversations

## Example Usage

```typescript
import { InboxSearchResponse } from "bereach/models/operations";

let value: InboxSearchResponse = {
  success: true,
  conversations: [
    {
      conversationUrn: "<value>",
      conversationUrl: "https://fond-replacement.info",
      lastActivityAt: 567072,
      createdAt: 461637,
      read: true,
      unreadCount: 446046,
      groupChat: true,
      participants: [
        {
          profileUrn: "<value>",
          firstName: "Rosalinda",
          lastName: "Schroeder",
          profileUrl: "https://noteworthy-testing.com/",
          headline: "<value>",
          profilePicture: "<value>",
          publicIdentifier: "<value>",
        },
      ],
      lastMessage: {
        text: "<value>",
        deliveredAt: 816412,
        senderProfileUrn: "<value>",
      },
    },
  ],
  nextCursor: "<value>",
  creditsUsed: 42645,
  retryAfter: 546872,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `conversations`                                                                                                                      | [operations.InboxSearchConversation](../../models/operations/inbox-search-conversation.md)[]                                         | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `nextCursor`                                                                                                                         | *string*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Cursor for fetching next page                                                                                                        |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.InboxSearchSpent](../../models/operations/inbox-search-spent.md)                                                         | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |