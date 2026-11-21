# ScheduledMessageListWhy

## Example Usage

```typescript
import { ScheduledMessageListWhy } from "bereach/models/operations";

let value: ScheduledMessageListWhy = {
  status: "window",
  detail: "<value>",
  position: 660815,
  opensAt: "<value>",
  clearsItself: true,
  fixUrl: "https://suburban-thyme.name/",
  kind: "<value>",
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `status`                                                                                                | [operations.FirstDmMessageStatus](../../models/operations/first-dm-message-status.md)                   | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `detail`                                                                                                | *string*                                                                                                | :heavy_check_mark:                                                                                      | Why it has not gone yet, in plain words.                                                                |
| `position`                                                                                              | *number*                                                                                                | :heavy_check_mark:                                                                                      | 1-based place in line when ready; null while set aside.                                                 |
| `opensAt`                                                                                               | *string*                                                                                                | :heavy_check_mark:                                                                                      | For `window`, when sending hours reopen; for `accepted`, when the pause before the first message lifts. |
| `clearsItself`                                                                                          | *boolean*                                                                                               | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `fixUrl`                                                                                                | *string*                                                                                                | :heavy_check_mark:                                                                                      | N/A                                                                                                     |
| `kind`                                                                                                  | *string*                                                                                                | :heavy_check_mark:                                                                                      | N/A                                                                                                     |