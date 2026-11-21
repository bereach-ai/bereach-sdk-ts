# WithdrawInvitationSpent

What this call spent, in money.

## Example Usage

```typescript
import { WithdrawInvitationSpent } from "bereach/models/operations";

let value: WithdrawInvitationSpent = {
  amount: 6476.15,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `amount`                                                                                         | *number*                                                                                         | :heavy_check_mark:                                                                               | The money spent.                                                                                 |
| `currency`                                                                                       | [operations.WithdrawInvitationCurrency](../../models/operations/withdraw-invitation-currency.md) | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `text`                                                                                           | *string*                                                                                         | :heavy_check_mark:                                                                               | The amount as a person reads it, with its currency.                                              |