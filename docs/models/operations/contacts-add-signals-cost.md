# ContactsAddSignalsCost

The most a run costs, in money: say this amount.

## Example Usage

```typescript
import { ContactsAddSignalsCost } from "bereach/models/operations";

let value: ContactsAddSignalsCost = {
  amount: 1015.35,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                   | *number*                                                                                                   | :heavy_check_mark:                                                                                         | The money spent.                                                                                           |
| `currency`                                                                                                 | [operations.ContactsAddSignalsCostCurrency](../../models/operations/contacts-add-signals-cost-currency.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `text`                                                                                                     | *string*                                                                                                   | :heavy_check_mark:                                                                                         | The amount as a person reads it, with its currency.                                                        |