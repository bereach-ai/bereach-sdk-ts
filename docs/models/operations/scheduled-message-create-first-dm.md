# ScheduledMessageCreateFirstDm

On a duplicate that was approved, the same report as `line`.

## Example Usage

```typescript
import { ScheduledMessageCreateFirstDm } from "bereach/models/operations";

let value: ScheduledMessageCreateFirstDm = {
  queued: 16656,
  requeued: 403813,
  alreadyQueued: 681467,
  held: 131203,
  skipped: [
    {
      contactId: "<id>",
      scheduledMessageId: "<id>",
      reason: "<value>",
    },
  ],
  invitesQueued: 569157,
  accounts: [
    "<value 1>",
  ],
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `queued`                                                                   | *number*                                                                   | :heavy_check_mark:                                                         | N/A                                                                        |
| `requeued`                                                                 | *number*                                                                   | :heavy_check_mark:                                                         | N/A                                                                        |
| `alreadyQueued`                                                            | *number*                                                                   | :heavy_check_mark:                                                         | N/A                                                                        |
| `held`                                                                     | *number*                                                                   | :heavy_check_mark:                                                         | N/A                                                                        |
| `skipped`                                                                  | [operations.FirstDmSkipped](../../models/operations/first-dm-skipped.md)[] | :heavy_check_mark:                                                         | N/A                                                                        |
| `invitesQueued`                                                            | *number*                                                                   | :heavy_check_mark:                                                         | N/A                                                                        |
| `accounts`                                                                 | *string*[]                                                                 | :heavy_check_mark:                                                         | N/A                                                                        |