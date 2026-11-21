# WorkspacePool

The pool as the workspace's plan reads it, present when the pool is metered

## Example Usage

```typescript
import { WorkspacePool } from "bereach/models/operations";

let value: WorkspacePool = {
  percentage: 6138.33,
  remainingPercentage: 5521.86,
  isUnlimited: true,
  periodEnd: "<value>",
  tier: "<value>",
  trial: false,
  remaining: 311755,
};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `percentage`                                                                                                       | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | Percentage of the allowance used, as in credits.percentage                                                         |
| `remainingPercentage`                                                                                              | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | 100 minus percentage, rounded to 2 decimal places                                                                  |
| `isUnlimited`                                                                                                      | *boolean*                                                                                                          | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `periodEnd`                                                                                                        | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | When the allowance next refills (first of next month, UTC), on a plan or trial; the free tier's gift never refills |
| `tier`                                                                                                             | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | The workspace's plan tier                                                                                          |
| `trial`                                                                                                            | *boolean*                                                                                                          | :heavy_check_mark:                                                                                                 | Whether the plan is a running trial                                                                                |
| `remaining`                                                                                                        | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | What can still be spent, as in credits.remaining                                                                   |