# ScheduledMessageUpdateRequest

## Example Usage

```typescript
import { ScheduledMessageUpdateRequest } from "bereach/models/operations";

let value: ScheduledMessageUpdateRequest = {
  messageId: "<id>",
};
```

## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `messageId`                                             | *string*                                                | :heavy_check_mark:                                      | Scheduled message id to edit                            |
| `message`                                               | *string*                                                | :heavy_minus_sign:                                      | New DM text                                             |
| `scheduledSendAt`                                       | *string*                                                | :heavy_minus_sign:                                      | Accepted and ignored: a first message has no send time. |