# InboxSearchConversation

## Example Usage

```typescript
import { InboxSearchConversation } from "bereach/models/operations";

let value: InboxSearchConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://sentimental-incandescence.com/",
  lastActivityAt: 536677,
  createdAt: 240119,
  read: true,
  unreadCount: 21369,
  groupChat: false,
  participants: [],
  lastMessage: {
    text: "<value>",
    deliveredAt: 816412,
    senderProfileUrn: "<value>",
  },
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `conversationUrn`                                                                          | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `conversationUrl`                                                                          | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `lastActivityAt`                                                                           | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `createdAt`                                                                                | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `read`                                                                                     | *boolean*                                                                                  | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `unreadCount`                                                                              | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `groupChat`                                                                                | *boolean*                                                                                  | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `participants`                                                                             | [operations.InboxSearchParticipant](../../models/operations/inbox-search-participant.md)[] | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `lastMessage`                                                                              | [operations.InboxSearchLastMessage](../../models/operations/inbox-search-last-message.md)  | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `lastReadAt`                                                                               | *number*                                                                                   | :heavy_minus_sign:                                                                         | Epoch ms this account last read the thread.                                                |
| `notificationStatus`                                                                       | *string*                                                                                   | :heavy_minus_sign:                                                                         | Whether the thread is active, muted or snoozed for this account.                           |