# ContactsCheckFitSpent

What the check in progress has spent so far, in money.

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