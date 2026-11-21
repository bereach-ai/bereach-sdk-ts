# FindEmailsSpent

What this call spent, in money.

## Example Usage

```typescript
import { FindEmailsSpent } from "bereach/models/operations";

let value: FindEmailsSpent = {
  amount: 1802.08,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `amount`                                                                         | *number*                                                                         | :heavy_check_mark:                                                               | The money spent.                                                                 |
| `currency`                                                                       | [operations.FindEmailsCurrency](../../models/operations/find-emails-currency.md) | :heavy_check_mark:                                                               | N/A                                                                              |
| `text`                                                                           | *string*                                                                         | :heavy_check_mark:                                                               | The amount as a person reads it, with its currency.                              |