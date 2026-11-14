# GetProfileSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { GetProfileSpent } from "bereach/models/operations";

let value: GetProfileSpent = {
  amount: 7284.54,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `amount`                                                                         | *number*                                                                         | :heavy_check_mark:                                                               | The money spent.                                                                 |
| `currency`                                                                       | [operations.GetProfileCurrency](../../models/operations/get-profile-currency.md) | :heavy_check_mark:                                                               | N/A                                                                              |
| `text`                                                                           | *string*                                                                         | :heavy_check_mark:                                                               | The amount as a person reads it, with its currency.                              |