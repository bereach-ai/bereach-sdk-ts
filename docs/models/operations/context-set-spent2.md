# ContextSetSpent2

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ContextSetSpent2 } from "bereach/models/operations";

let value: ContextSetSpent2 = {
  amount: 6760.41,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `amount`                                                                           | *number*                                                                           | :heavy_check_mark:                                                                 | The money spent.                                                                   |
| `currency`                                                                         | [operations.ContextSetCurrency2](../../models/operations/context-set-currency2.md) | :heavy_check_mark:                                                                 | N/A                                                                                |
| `text`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | The amount as a person reads it, with its currency.                                |