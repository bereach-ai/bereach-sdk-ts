# ScheduledMessageCreateInvite

Where this person's connection request stands, from the invitation lane's own projection. Present on connection_request rows.

## Example Usage

```typescript
import { ScheduledMessageCreateInvite } from "bereach/models/operations";

let value: ScheduledMessageCreateInvite = {
  status: "window",
  detail: "<value>",
  clearsItself: false,
  fixUrl: "https://understated-fax.biz/",
  kind: "<value>",
  opensAt: "<value>",
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `status`                                                                                              | [operations.ScheduledMessageInviteStatus](../../models/operations/scheduled-message-invite-status.md) | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `detail`                                                                                              | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `clearsItself`                                                                                        | *boolean*                                                                                             | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `fixUrl`                                                                                              | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `kind`                                                                                                | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `opensAt`                                                                                             | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |