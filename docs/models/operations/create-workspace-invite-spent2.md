# CreateWorkspaceInviteSpent2

What this call spent, in money.

## Example Usage

```typescript
import { CreateWorkspaceInviteSpent2 } from "bereach/models/operations";

let value: CreateWorkspaceInviteSpent2 = {
  amount: 2228.79,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                  | *number*                                                                                                  | :heavy_check_mark:                                                                                        | The money spent.                                                                                          |
| `currency`                                                                                                | [operations.CreateWorkspaceInviteCurrency2](../../models/operations/create-workspace-invite-currency2.md) | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `text`                                                                                                    | *string*                                                                                                  | :heavy_check_mark:                                                                                        | The amount as a person reads it, with its currency.                                                       |