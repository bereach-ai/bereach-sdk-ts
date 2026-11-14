# PlanSearchesResponseBody2

## Example Usage

```typescript
import { PlanSearchesResponseBody2 } from "bereach/models/operations";

let value: PlanSearchesResponseBody2 = {
  planId: "<id>",
  version: 651469,
  ready: true,
  assumptions: [],
  questions: [
    {
      id: "<id>",
      question: "<value>",
      options: [],
    },
  ],
  segments: [
    {
      id: "<id>",
      name: "<value>",
      confidence: "low",
      kinds: [
        "<value 1>",
        "<value 2>",
        "<value 3>",
      ],
      places: [
        "<value 1>",
      ],
      groups: [
        {
          id: "<id>",
          name: "<value>",
        },
      ],
      evidence: [
        {
          source: "<value>",
          quote: "<value>",
        },
      ],
    },
  ],
  searches: [
    {
      id: "<id>",
      segment: "<value>",
      language: "<value>",
      where: "<value>",
      queries: [
        "<value 1>",
        "<value 2>",
      ],
    },
  ],
  peopleUpTo: 380902,
  costEstimateCredits: 96275,
  costLikelyCredits: 156052,
  next: "<value>",
};
```

## Fields

| Field                                                                                                            | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `planId`                                                                                                         | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `version`                                                                                                        | *number*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `ready`                                                                                                          | *true*                                                                                                           | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `assumptions`                                                                                                    | [operations.Assumption2](../../models/operations/assumption2.md)[]                                               | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `questions`                                                                                                      | [operations.Question2](../../models/operations/question2.md)[]                                                   | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `segments`                                                                                                       | [operations.Segment2](../../models/operations/segment2.md)[]                                                     | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `searches`                                                                                                       | [operations.PlanSearchesSearch2](../../models/operations/plan-searches-search2.md)[]                             | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `peopleUpTo`                                                                                                     | *number*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |
| `costEstimateCredits`                                                                                            | *number*                                                                                                         | :heavy_check_mark:                                                                                               | The most the run may spend, in credits, for code: tell the user cost_estimate.                                   |
| `costLikelyCredits`                                                                                              | *number*                                                                                                         | :heavy_check_mark:                                                                                               | What the run usually spends when the market holds the people, in credits, for code: tell the user cost_likely.   |
| `costEstimate`                                                                                                   | [operations.PlanSearchesCostEstimate](../../models/operations/plan-searches-cost-estimate.md)                    | :heavy_minus_sign:                                                                                               | The most the run may spend, in money at the workspace's rate: the figure to tell the user. It never spends more. |
| `costLikely`                                                                                                     | [operations.CostLikely](../../models/operations/cost-likely.md)                                                  | :heavy_minus_sign:                                                                                               | What the run usually spends when the market holds the people, in money: the figure to tell the user.             |
| `heldBack`                                                                                                       | [operations.HeldBack](../../models/operations/held-back.md)                                                      | :heavy_minus_sign:                                                                                               | Searches and query lines kept out of the plan to fit its bounds or the pool, ready to add.                       |
| `unread`                                                                                                         | [operations.Unread2](../../models/operations/unread2.md)[]                                                       | :heavy_minus_sign:                                                                                               | N/A                                                                                                              |
| `next`                                                                                                           | *string*                                                                                                         | :heavy_check_mark:                                                                                               | N/A                                                                                                              |