# ContactsAddSpent

What this call spent, in money.

## Example Usage

```typescript
import { ContactsAddSpent } from "bereach/models/operations";

let value: ContactsAddSpent = {
  amount: 2922.88,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `amount`                                                                           | *number*                                                                           | :heavy_check_mark:                                                                 | The money spent.                                                                   |
| `currency`                                                                         | [operations.ContactsAddCurrency](../../models/operations/contacts-add-currency.md) | :heavy_check_mark:                                                                 | N/A                                                                                |
| `text`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | The amount as a person reads it, with its currency.                                |