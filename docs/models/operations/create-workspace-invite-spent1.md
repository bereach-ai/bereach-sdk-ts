# CreateWorkspaceInviteSpent1

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { CreateWorkspaceInviteSpent1 } from "bereach/models/operations";

let value: CreateWorkspaceInviteSpent1 = {
  amount: 8532.4,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                  | *number*                                                                                                  | :heavy_check_mark:                                                                                        | The money spent.                                                                                          |
| `currency`                                                                                                | [operations.CreateWorkspaceInviteCurrency1](../../models/operations/create-workspace-invite-currency1.md) | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `text`                                                                                                    | *string*                                                                                                  | :heavy_check_mark:                                                                                        | The amount as a person reads it, with its currency.                                                       |