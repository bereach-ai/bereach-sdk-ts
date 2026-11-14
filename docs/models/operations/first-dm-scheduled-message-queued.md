# FirstDmScheduledMessageQueued

## Example Usage

```typescript
import { FirstDmScheduledMessageQueued } from "bereach/models/operations";

let value: FirstDmScheduledMessageQueued = {
  kind: "queued",
  scheduledMessageId: "<id>",
  why: {
    status: "accepted",
    detail: "<value>",
    position: 15508,
    opensAt: "<value>",
    clearsItself: false,
    fixUrl: "https://formal-annual.name",
    kind: "<value>",
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `kind`                                                                                          | *"queued"*                                                                                      | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `scheduledMessageId`                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `why`                                                                                           | [operations.ScheduledMessageCreateWhy](../../models/operations/scheduled-message-create-why.md) | :heavy_check_mark:                                                                              | N/A                                                                                             |