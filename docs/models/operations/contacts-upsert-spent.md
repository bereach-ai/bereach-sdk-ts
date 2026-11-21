# ContactsUpsertSpent

What this call spent, in money.

## Example Usage

```typescript
import { ContactsUpsertSpent } from "bereach/models/operations";

let value: ContactsUpsertSpent = {
  amount: 9715.98,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `amount`                                                                                 | *number*                                                                                 | :heavy_check_mark:                                                                       | The money spent.                                                                         |
| `currency`                                                                               | [operations.ContactsUpsertCurrency](../../models/operations/contacts-upsert-currency.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `text`                                                                                   | *string*                                                                                 | :heavy_check_mark:                                                                       | The amount as a person reads it, with its currency.                                      |