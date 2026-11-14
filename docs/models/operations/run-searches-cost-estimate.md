# RunSearchesCostEstimate

The most this run may spend, in money: the plan's ceiling, the figure to tell the user.

## Example Usage

```typescript
import { RunSearchesCostEstimate } from "bereach/models/operations";

let value: RunSearchesCostEstimate = {
  amount: 935.14,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `amount`                                                                                                     | *number*                                                                                                     | :heavy_check_mark:                                                                                           | The money spent.                                                                                             |
| `currency`                                                                                                   | [operations.RunSearchesCostEstimateCurrency](../../models/operations/run-searches-cost-estimate-currency.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `text`                                                                                                       | *string*                                                                                                     | :heavy_check_mark:                                                                                           | The amount as a person reads it, with its currency.                                                          |