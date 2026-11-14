# RunSearchesSpent

What this run has spent so far, in money, over every call on this plan_id: the figure to tell the user.

## Example Usage

```typescript
import { RunSearchesSpent } from "bereach/models/operations";

let value: RunSearchesSpent = {
  amount: 7822.42,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `amount`                                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | The money spent.                                                                              |
| `currency`                                                                                    | [operations.RunSearchesSpentCurrency](../../models/operations/run-searches-spent-currency.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `text`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | The amount as a person reads it, with its currency.                                           |