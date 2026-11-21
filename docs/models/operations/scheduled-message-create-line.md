# ScheduledMessageCreateLine

What approving did, present when the request asked for approval: messages that entered the line, were put back or were already there, and the rows the line would not take.

## Example Usage

```typescript
import { ScheduledMessageCreateLine } from "bereach/models/operations";

let value: ScheduledMessageCreateLine = {
  queued: 741006,
  requeued: 859994,
  alreadyQueued: 193224,
  skipped: [
    {
      contactId: "<id>",
      scheduledMessageId: "<id>",
      reason: "<value>",
    },
  ],
  invitesQueued: 850215,
  accounts: [
    "<value 1>",
    "<value 2>",
  ],
};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `queued`                                                                                                           | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `requeued`                                                                                                         | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `alreadyQueued`                                                                                                    | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `skipped`                                                                                                          | [operations.ScheduledMessageCreateLineSkipped](../../models/operations/scheduled-message-create-line-skipped.md)[] | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `invitesQueued`                                                                                                    | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `accounts`                                                                                                         | *string*[]                                                                                                         | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |