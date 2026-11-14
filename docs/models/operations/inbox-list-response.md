# InboxListResponse

Inbox conversations

## Example Usage

```typescript
import { InboxListResponse } from "bereach/models/operations";

let value: InboxListResponse = {
  success: true,
  conversations: [
    {
      conversationUrn: "<value>",
      conversationUrl: "https://queasy-gray.biz",
      lastActivityAt: 291893,
      createdAt: 237397,
      read: true,
      unreadCount: 274144,
      groupChat: false,
      participants: [
        {
          profileUrn: "<value>",
          firstName: "Casimir",
          lastName: "Champlin",
          profileUrl: null,
          headline: "<value>",
          profilePicture: "<value>",
          publicIdentifier: "<value>",
        },
      ],
      lastMessage: {
        text: null,
        deliveredAt: 441255,
        senderProfileUrn: "<value>",
      },
    },
  ],
  nextCursor: "<value>",
  creditsUsed: 630398,
  retryAfter: 801573,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `conversations`                                                                                                                      | [operations.InboxListConversation](../../models/operations/inbox-list-conversation.md)[]                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `nextCursor`                                                                                                                         | *string*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Cursor for fetching next page                                                                                                        |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.InboxListSpent](../../models/operations/inbox-list-spent.md)                                                             | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |