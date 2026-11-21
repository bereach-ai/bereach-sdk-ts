# GetConnectionStatusHolding

This account's own schedule, not a fault and never a limit: it is waiting for its sending hours, or for the gap between two invitations. Nothing is wrong and nobody needs to act. Null when it can send right now, and null when something IS wrong, which is blocked. Report it as a wait with a time, never as a problem.

## Example Usage

```typescript
import { GetConnectionStatusHolding } from "bereach/models/operations";

let value: GetConnectionStatusHolding = {
  kind: "paced",
  message: "<value>",
  resumesAt: "<value>",
  clearsItself: true,
  fixUrl: null,
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `kind`                                                                                                     | [operations.GetConnectionStatusHoldingKind](../../models/operations/get-connection-status-holding-kind.md) | :heavy_check_mark:                                                                                         | outside_window is this account's sending hours; paced is the gap between two invitations.                  |
| `message`                                                                                                  | *string*                                                                                                   | :heavy_check_mark:                                                                                         | A plain sentence explaining it, suitable to show as written                                                |
| `resumesAt`                                                                                                | *string*                                                                                                   | :heavy_check_mark:                                                                                         | When sending resumes, without anybody doing anything                                                       |
| `clearsItself`                                                                                             | *true*                                                                                                     | :heavy_check_mark:                                                                                         | Always true. This is a schedule, so time alone clears it.                                                  |
| `fixUrl`                                                                                                   | *null*                                                                                                     | :heavy_check_mark:                                                                                         | Always null. There is nothing to fix and nowhere to send anybody.                                          |