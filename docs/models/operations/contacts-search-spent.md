# ContactsSearchSpent

What this call spent, in money.

## Example Usage

```typescript
import { ContactsSearchSpent } from "bereach/models/operations";

let value: ContactsSearchSpent = {
  amount: 9853.65,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `amount`                                                                                 | *number*                                                                                 | :heavy_check_mark:                                                                       | The money spent.                                                                         |
| `currency`                                                                               | [operations.ContactsSearchCurrency](../../models/operations/contacts-search-currency.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `text`                                                                                   | *string*                                                                                 | :heavy_check_mark:                                                                       | The amount as a person reads it, with its currency.                                      |