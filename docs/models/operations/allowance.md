# Allowance

What the plan, the trial or the free tier includes: held by the five-hour usage limit and, on a trial, its cap

## Example Usage

```typescript
import { Allowance } from "bereach/models/operations";

let value: Allowance = {
  window: {
    usedPercent: 3928.3,
    resetsAt: "<value>",
  },
  trialCap: {
    usedPercent: 7435.5,
  },
  heldBy: null,
  left: true,
};
```

## Fields

| Field                                                                                                                                                         | Type                                                                                                                                                          | Required                                                                                                                                                      | Description                                                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `window`                                                                                                                                                      | [operations.Window](../../models/operations/window.md)                                                                                                        | :heavy_check_mark:                                                                                                                                            | The five-hour usage limit on paid reads, on a trial, a plan or the free tier                                                                                  |
| `trialCap`                                                                                                                                                    | [operations.TrialCap](../../models/operations/trial-cap.md)                                                                                                   | :heavy_check_mark:                                                                                                                                            | The trial's cap, on a running trial; null otherwise                                                                                                           |
| `heldBy`                                                                                                                                                      | [operations.HeldBy](../../models/operations/held-by.md)                                                                                                       | :heavy_check_mark:                                                                                                                                            | The limit holding the allowance now, or null. While one holds, paid reads are paid from the money added by card alone, and stop when too little of it is left |
| `left`                                                                                                                                                        | *boolean*                                                                                                                                                     | :heavy_check_mark:                                                                                                                                            | Whether anything included is left this period; false on pay as you go, where paid reads are paid from the money added and no limit holds them                 |