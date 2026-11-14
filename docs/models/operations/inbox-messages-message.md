# InboxMessagesMessage

## Example Usage

```typescript
import { InboxMessagesMessage } from "bereach/models/operations";

let value: InboxMessagesMessage = {
  messageUrn: "<value>",
  text: "<value>",
  deliveredAt: 757645,
  senderProfileUrn: "<value>",
  sender: {
    firstName: "Buck",
    lastName: "Yundt",
    profileUrl: null,
    headline: "<value>",
    profilePicture: "<value>",
    publicIdentifier: "<value>",
    profileUrn: "<value>",
  },
  attachments: [],
  isOutbound: true,
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `messageUrn`                                                                                 | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `text`                                                                                       | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `deliveredAt`                                                                                | *number*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `senderProfileUrn`                                                                           | *string*                                                                                     | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `sender`                                                                                     | [operations.InboxMessagesSender](../../models/operations/inbox-messages-sender.md)           | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `attachments`                                                                                | [operations.InboxMessagesAttachment](../../models/operations/inbox-messages-attachment.md)[] | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `isOutbound`                                                                                 | *boolean*                                                                                    | :heavy_check_mark:                                                                           | True if the authenticated user sent this message.                                            |