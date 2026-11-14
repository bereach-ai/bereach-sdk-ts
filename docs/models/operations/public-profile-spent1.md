# PublicProfileSpent1

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { PublicProfileSpent1 } from "bereach/models/operations";

let value: PublicProfileSpent1 = {
  amount: 8257.09,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `amount`                                                                                 | *number*                                                                                 | :heavy_check_mark:                                                                       | The money spent.                                                                         |
| `currency`                                                                               | [operations.PublicProfileCurrency1](../../models/operations/public-profile-currency1.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `text`                                                                                   | *string*                                                                                 | :heavy_check_mark:                                                                       | The amount as a person reads it, with its currency.                                      |