# ConnectProfileSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ConnectProfileSpent } from "bereach/models/operations";

let value: ConnectProfileSpent = {
  amount: 6967.58,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `amount`                                                                                 | *number*                                                                                 | :heavy_check_mark:                                                                       | The money spent.                                                                         |
| `currency`                                                                               | [operations.ConnectProfileCurrency](../../models/operations/connect-profile-currency.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `text`                                                                                   | *string*                                                                                 | :heavy_check_mark:                                                                       | The amount as a person reads it, with its currency.                                      |