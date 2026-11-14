# ContactsCheckFitSpent

What the check in progress has spent so far, in money: the figure to tell the user.

## Example Usage

```typescript
import { ContactsCheckFitSpent } from "bereach/models/operations";

let value: ContactsCheckFitSpent = {
  amount: 7493.94,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                 | *number*                                                                                                 | :heavy_check_mark:                                                                                       | The money spent.                                                                                         |
| `currency`                                                                                               | [operations.ContactsCheckFitSpentCurrency](../../models/operations/contacts-check-fit-spent-currency.md) | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `text`                                                                                                   | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The amount as a person reads it, with its currency.                                                      |