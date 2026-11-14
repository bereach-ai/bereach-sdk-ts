# GetCreditsResponse

Credit balance for the workspace

## Example Usage

```typescript
import { GetCreditsResponse } from "bereach/models/operations";

let value: GetCreditsResponse = {
  success: true,
  credits: {
    current: 284087,
    limit: 104219,
    remaining: 714218,
    topUp: 164647,
    topUpRate: "pro",
    percentage: 6256,
    isUnlimited: true,
    currency: "EUR",
  },
  limits: {
    allowance: {
      window: {
        usedPercent: 3928.3,
        resetsAt: "<value>",
      },
      trialCap: {
        usedPercent: 7435.5,
      },
      heldBy: "window",
      left: true,
    },
    topUp: {
      left: true,
      limited: false,
    },
    topUpUrl: "https://new-prohibition.org",
    note: "<value>",
  },
  creditsUsed: 18112,
  retryAfter: 918941,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `credits`                                                                                                                                 | [operations.Credits](../../models/operations/credits.md)                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `workspacePool`                                                                                                                           | [operations.WorkspacePool](../../models/operations/workspace-pool.md)                                                                     | :heavy_minus_sign:                                                                                                                        | The pool as the workspace's plan reads it, present when the pool is metered                                                               |
| `limits`                                                                                                                                  | [operations.GetCreditsLimits](../../models/operations/get-credits-limits.md)                                                              | :heavy_check_mark:                                                                                                                        | The two buckets: the included use, held by the five-hour usage limit and a trial's cap, and the money added by card, which no limit holds |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged.      |
| `spent`                                                                                                                                   | [operations.GetCreditsSpent](../../models/operations/get-credits-spent.md)                                                                | :heavy_minus_sign:                                                                                                                        | What this call spent, in money: the figure to tell the user, written as text says it.                                                     |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |