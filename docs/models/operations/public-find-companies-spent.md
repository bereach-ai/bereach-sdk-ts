# PublicFindCompaniesSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { PublicFindCompaniesSpent } from "bereach/models/operations";

let value: PublicFindCompaniesSpent = {
  amount: 8231.6,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `amount`                                                                                            | *number*                                                                                            | :heavy_check_mark:                                                                                  | The money spent.                                                                                    |
| `currency`                                                                                          | [operations.PublicFindCompaniesCurrency](../../models/operations/public-find-companies-currency.md) | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `text`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | The amount as a person reads it, with its currency.                                                 |