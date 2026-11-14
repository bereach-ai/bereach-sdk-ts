# ContextSetSpent1

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ContextSetSpent1 } from "bereach/models/operations";

let value: ContextSetSpent1 = {
  amount: 6201.76,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `amount`                                                                           | *number*                                                                           | :heavy_check_mark:                                                                 | The money spent.                                                                   |
| `currency`                                                                         | [operations.ContextSetCurrency1](../../models/operations/context-set-currency1.md) | :heavy_check_mark:                                                                 | N/A                                                                                |
| `text`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | The amount as a person reads it, with its currency.                                |