# ContactsCheckFitCost

The most a check costs, in money: say this amount.

## Example Usage

```typescript
import { ContactsCheckFitCost } from "bereach/models/operations";

let value: ContactsCheckFitCost = {
  amount: 4991.13,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `amount`                                                                                               | *number*                                                                                               | :heavy_check_mark:                                                                                     | The money spent.                                                                                       |
| `currency`                                                                                             | [operations.ContactsCheckFitCostCurrency](../../models/operations/contacts-check-fit-cost-currency.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `text`                                                                                                 | *string*                                                                                               | :heavy_check_mark:                                                                                     | The amount as a person reads it, with its currency.                                                    |