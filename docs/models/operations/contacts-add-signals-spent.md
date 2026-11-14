# ContactsAddSignalsSpent

What the run in progress has spent so far, in money: the figure to tell the user.

## Example Usage

```typescript
import { ContactsAddSignalsSpent } from "bereach/models/operations";

let value: ContactsAddSignalsSpent = {
  amount: 5207.15,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `amount`                                                                                                     | *number*                                                                                                     | :heavy_check_mark:                                                                                           | The money spent.                                                                                             |
| `currency`                                                                                                   | [operations.ContactsAddSignalsSpentCurrency](../../models/operations/contacts-add-signals-spent-currency.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `text`                                                                                                       | *string*                                                                                                     | :heavy_check_mark:                                                                                           | The amount as a person reads it, with its currency.                                                          |