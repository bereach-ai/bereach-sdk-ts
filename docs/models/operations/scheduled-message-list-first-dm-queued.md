# ScheduledMessageListFirstDmQueued

## Example Usage

```typescript
import { ScheduledMessageListFirstDmQueued } from "bereach/models/operations";

let value: ScheduledMessageListFirstDmQueued = {
  kind: "queued",
  scheduledMessageId: "<id>",
  why: {
    status: "not-on-list",
    detail: "<value>",
    position: 631546,
    opensAt: "<value>",
    clearsItself: true,
    fixUrl: "https://jealous-collectivization.info/",
    kind: "<value>",
  },
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `kind`                                                                                      | *"queued"*                                                                                  | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `scheduledMessageId`                                                                        | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `why`                                                                                       | [operations.ScheduledMessageListWhy](../../models/operations/scheduled-message-list-why.md) | :heavy_check_mark:                                                                          | N/A                                                                                         |