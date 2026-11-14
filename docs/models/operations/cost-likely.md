# CostLikely

What the run usually spends when the market holds the people, in money: the figure to tell the user.

## Example Usage

```typescript
import { CostLikely } from "bereach/models/operations";

let value: CostLikely = {
  amount: 9452.6,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `amount`                                                                         | *number*                                                                         | :heavy_check_mark:                                                               | The money spent.                                                                 |
| `currency`                                                                       | [operations.CostLikelyCurrency](../../models/operations/cost-likely-currency.md) | :heavy_check_mark:                                                               | N/A                                                                              |
| `text`                                                                           | *string*                                                                         | :heavy_check_mark:                                                               | The amount as a person reads it, with its currency.                              |