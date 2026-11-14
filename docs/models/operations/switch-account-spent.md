# SwitchAccountSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { SwitchAccountSpent } from "bereach/models/operations";

let value: SwitchAccountSpent = {
  amount: 7792.43,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `amount`                                                                               | *number*                                                                               | :heavy_check_mark:                                                                     | The money spent.                                                                       |
| `currency`                                                                             | [operations.SwitchAccountCurrency](../../models/operations/switch-account-currency.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `text`                                                                                 | *string*                                                                               | :heavy_check_mark:                                                                     | The amount as a person reads it, with its currency.                                    |