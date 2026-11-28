# InboxListConversation

## Example Usage

```typescript
import { InboxListConversation } from "bereach/models/operations";

let value: InboxListConversation = {
  conversationUrn: "<value>",
  conversationUrl: "https://weighty-rim.info/",
  lastActivityAt: 99482,
  createdAt: 565920,
  read: false,
  unreadCount: 289524,
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
  lastMessage: null,
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                      | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `conversationUrl`                                                                      | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `lastActivityAt`                                                                       | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `createdAt`                                                                            | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `read`                                                                                 | *boolean*                                                                              | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `unreadCount`                                                                          | *number*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `groupChat`                                                                            | *boolean*                                                                              | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `participants`                                                                         | [operations.InboxListParticipant](../../models/operations/inbox-list-participant.md)[] | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `lastMessage`                                                                          | [operations.InboxListLastMessage](../../models/operations/inbox-list-last-message.md)  | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `lastReadAt`                                                                           | *number*                                                                               | :heavy_minus_sign:                                                                     | Epoch ms this account last read the thread.                                            |
| `notificationStatus`                                                                   | *string*                                                                               | :heavy_minus_sign:                                                                     | Whether the thread is active, muted or snoozed for this account.                       |