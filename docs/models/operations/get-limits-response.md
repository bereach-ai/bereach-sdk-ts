# GetLimitsResponse

Rate limit status for all action types

## Example Usage

```typescript
import { GetLimitsResponse } from "bereach/models/operations";

let value: GetLimitsResponse = {
  success: true,
  multiplier: 6690.82,
  limits: {
    connectionRequest: {
      uncapped: true,
      daily: null,
      weekly: {
        current: 905903,
        limit: 617573,
        remaining: 804803,
      },
      minIntervalSeconds: 426412,
      nextResetDaily: "<value>",
      nextResetWeekly: "<value>",
    },
    message: {
      uncapped: false,
      daily: {
        current: 567882,
        limit: 669069,
        remaining: 636753,
      },
      weekly: {
        current: 534020,
        limit: 472297,
        remaining: 863521,
      },
      minIntervalSeconds: 48135,
      nextResetDaily: "<value>",
      nextResetWeekly: "<value>",
    },
    profileVisit: {
      uncapped: false,
      daily: {
        current: 293170,
        limit: 692882,
        remaining: 96344,
      },
      weekly: {
        current: 791982,
        limit: 483792,
        remaining: 394394,
      },
      minIntervalSeconds: 440440,
      nextResetDaily: null,
      nextResetWeekly: "<value>",
    },
    scraping: {
      uncapped: false,
      daily: {
        current: 137081,
        limit: 85944,
        remaining: 814423,
      },
      weekly: null,
      minIntervalSeconds: 811262,
      nextResetDaily: null,
      nextResetWeekly: "<value>",
    },
  },
  creditsUsed: 114833,
  retryAfter: 792378,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `multiplier`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Workspace limit multiplier applied to all base limits (default 1.0)                                                                  |
| `limits`                                                                                                                             | [operations.GetLimitsLimits](../../models/operations/get-limits-limits.md)                                                           | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.GetLimitsSpent](../../models/operations/get-limits-spent.md)                                                             | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |