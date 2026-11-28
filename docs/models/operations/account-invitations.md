# AccountInvitations

## Example Usage

```typescript
import { AccountInvitations } from "bereach/models/operations";

let value: AccountInvitations = {
  from: "<value>",
  to: "<value>",
  days: "every day",
  nextOpensAt: "<value>",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `from`                                                                                      | *string*                                                                                    | :heavy_check_mark:                                                                          | When connection requests start, local time in timeZone.                                     |
| `to`                                                                                        | *string*                                                                                    | :heavy_check_mark:                                                                          | When they stop, local time in timeZone; nothing goes out from this minute on.               |
| `days`                                                                                      | [operations.GetConnectionStatusDays](../../models/operations/get-connection-status-days.md) | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `nextOpensAt`                                                                               | *string*                                                                                    | :heavy_check_mark:                                                                          | When the hours next open, in UTC. Null while they are open now.                             |