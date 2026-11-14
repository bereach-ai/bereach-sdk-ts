# GetConnectionStatusBlocked

Set only while something is stopping this account. Never set for the ordinary spacing between two invitations, which is not a fault: that is state 'spacing'. If this is null, nothing is wrong with the account.

## Example Usage

```typescript
import { GetConnectionStatusBlocked } from "bereach/models/operations";

let value: GetConnectionStatusBlocked = {
  kind: "challenge",
  message: "<value>",
  resumesAt: "<value>",
  clearsItself: true,
  fixUrl: "https://striking-morning.biz/",
};
```

## Fields

| Field                                                                                                            | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `kind`                                                                                                           | [operations.BlockedKind](../../models/operations/blocked-kind.md)                                                | :heavy_check_mark:                                                                                               | Why nothing is going out. The ordinary spacing between two invitations is state 'spacing', never a block.        |
| `message`                                                                                                        | *string*                                                                                                         | :heavy_check_mark:                                                                                               | A plain sentence explaining it, suitable to show as written                                                      |
| `resumesAt`                                                                                                      | *string*                                                                                                         | :heavy_check_mark:                                                                                               | When it lifts. Null when it needs a person to act rather than time to pass.                                      |
| `clearsItself`                                                                                                   | *boolean*                                                                                                        | :heavy_check_mark:                                                                                               | Whether waiting is enough, or somebody has to do something                                                       |
| `fixUrl`                                                                                                         | *string*                                                                                                         | :heavy_check_mark:                                                                                               | Where to send the account owner to fix it, when a person has to act. Null for the kinds that clear on their own. |