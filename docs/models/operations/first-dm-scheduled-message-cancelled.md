# FirstDmScheduledMessageCancelled

## Example Usage

```typescript
import { FirstDmScheduledMessageCancelled } from "bereach/models/operations";

let value: FirstDmScheduledMessageCancelled = {
  kind: "cancelled",
  scheduledMessageId: "<id>",
  reason: "<value>",
};
```

## Fields

| Field                | Type                 | Required             | Description          |
| -------------------- | -------------------- | -------------------- | -------------------- |
| `kind`               | *"cancelled"*        | :heavy_check_mark:   | N/A                  |
| `scheduledMessageId` | *string*             | :heavy_check_mark:   | N/A                  |
| `reason`             | *string*             | :heavy_check_mark:   | N/A                  |