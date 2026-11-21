# FindPhonesSpent

What this call spent, in money.

## Example Usage

```typescript
import { FindPhonesSpent } from "bereach/models/operations";

let value: FindPhonesSpent = {
  amount: 8724.19,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `amount`                                                                         | *number*                                                                         | :heavy_check_mark:                                                               | The money spent.                                                                 |
| `currency`                                                                       | [operations.FindPhonesCurrency](../../models/operations/find-phones-currency.md) | :heavy_check_mark:                                                               | N/A                                                                              |
| `text`                                                                           | *string*                                                                         | :heavy_check_mark:                                                               | The amount as a person reads it, with its currency.                              |