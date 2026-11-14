# FindConversationResponse

Conversation found (or not)

## Example Usage

```typescript
import { FindConversationResponse } from "bereach/models/operations";

let value: FindConversationResponse = {
  success: true,
  found: false,
  conversation: {
    conversationUrn: "<value>",
  },
  messages: null,
  creditsUsed: 264766,
  retryAfter: 856891,
};
```

## Fields

| Field                                                                                                                                      | Type                                                                                                                                       | Required                                                                                                                                   | Description                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                                  | *true*                                                                                                                                     | :heavy_check_mark:                                                                                                                         | N/A                                                                                                                                        |
| `found`                                                                                                                                    | *boolean*                                                                                                                                  | :heavy_check_mark:                                                                                                                         | N/A                                                                                                                                        |
| `conversation`                                                                                                                             | [operations.FindConversationConversation](../../models/operations/find-conversation-conversation.md)                                       | :heavy_check_mark:                                                                                                                         | Lightweight conversation reference (O(1) lookup returns URN only, not full details).                                                       |
| `messages`                                                                                                                                 | [operations.FindConversationMessage](../../models/operations/find-conversation-message.md)[]                                               | :heavy_check_mark:                                                                                                                         | N/A                                                                                                                                        |
| `prevCursor`                                                                                                                               | *number*                                                                                                                                   | :heavy_minus_sign:                                                                                                                         | deliveredAt timestamp (ms) of the oldest message: pass as 'deliveredAt' to load older messages. Only present when includeMessages is true. |
| `userProfileUrn`                                                                                                                           | *string*                                                                                                                                   | :heavy_minus_sign:                                                                                                                         | The authenticated user's profile URN. Useful for determining message direction.                                                            |
| `creditsUsed`                                                                                                                              | *number*                                                                                                                                   | :heavy_check_mark:                                                                                                                         | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged.       |
| `spent`                                                                                                                                    | [operations.FindConversationSpent](../../models/operations/find-conversation-spent.md)                                                     | :heavy_minus_sign:                                                                                                                         | What this call spent, in money: the figure to tell the user, written as text says it.                                                      |
| `retryAfter`                                                                                                                               | *number*                                                                                                                                   | :heavy_check_mark:                                                                                                                         | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                           |