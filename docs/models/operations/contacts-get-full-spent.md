# ContactsGetFullSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ContactsGetFullSpent } from "bereach/models/operations";

let value: ContactsGetFullSpent = {
  amount: 1516.39,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `amount`                                                                                    | *number*                                                                                    | :heavy_check_mark:                                                                          | The money spent.                                                                            |
| `currency`                                                                                  | [operations.ContactsGetFullCurrency](../../models/operations/contacts-get-full-currency.md) | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `text`                                                                                      | *string*                                                                                    | :heavy_check_mark:                                                                          | The amount as a person reads it, with its currency.                                         |