# ContactsGetByUrlSpent

What this call spent, in money.

## Example Usage

```typescript
import { ContactsGetByUrlSpent } from "bereach/models/operations";

let value: ContactsGetByUrlSpent = {
  amount: 6168.24,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `amount`                                                                                       | *number*                                                                                       | :heavy_check_mark:                                                                             | The money spent.                                                                               |
| `currency`                                                                                     | [operations.ContactsGetByUrlCurrency](../../models/operations/contacts-get-by-url-currency.md) | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `text`                                                                                         | *string*                                                                                       | :heavy_check_mark:                                                                             | The amount as a person reads it, with its currency.                                            |