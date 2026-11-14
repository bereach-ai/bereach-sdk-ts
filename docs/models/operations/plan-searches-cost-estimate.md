# PlanSearchesCostEstimate

The most the run may spend, in money at the workspace's rate: the figure to tell the user. It never spends more.

## Example Usage

```typescript
import { PlanSearchesCostEstimate } from "bereach/models/operations";

let value: PlanSearchesCostEstimate = {
  amount: 1108.81,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                       | *number*                                                                                                       | :heavy_check_mark:                                                                                             | The money spent.                                                                                               |
| `currency`                                                                                                     | [operations.PlanSearchesCostEstimateCurrency](../../models/operations/plan-searches-cost-estimate-currency.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `text`                                                                                                         | *string*                                                                                                       | :heavy_check_mark:                                                                                             | The amount as a person reads it, with its currency.                                                            |