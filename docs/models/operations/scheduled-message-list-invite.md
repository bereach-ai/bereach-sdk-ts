# ScheduledMessageListInvite

Where this person's connection request stands, from the invitation lane's own projection. Present on connection_request rows.

## Example Usage

```typescript
import { ScheduledMessageListInvite } from "bereach/models/operations";

let value: ScheduledMessageListInvite = {
  status: "blocked",
  detail: "<value>",
  clearsItself: true,
  fixUrl: "https://steel-providence.net",
  kind: "<value>",
  opensAt: null,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `status`                                                                           | [operations.MessageInviteStatus](../../models/operations/message-invite-status.md) | :heavy_check_mark:                                                                 | N/A                                                                                |
| `detail`                                                                           | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `clearsItself`                                                                     | *boolean*                                                                          | :heavy_check_mark:                                                                 | N/A                                                                                |
| `fixUrl`                                                                           | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `kind`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `opensAt`                                                                          | *string*                                                                           | :heavy_check_mark:                                                                 | N/A                                                                                |