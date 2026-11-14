# PlanSearchesResponseBody1

## Example Usage

```typescript
import { PlanSearchesResponseBody1 } from "bereach/models/operations";

let value: PlanSearchesResponseBody1 = {
  planId: "<id>",
  version: 449173,
  ready: false,
  assumptions: [
    {
      fact: "<value>",
      origin: "inferred",
      source: "<value>",
      use: "search",
      applied: true,
    },
  ],
  questions: [],
  segments: [],
  searches: [
    {
      id: "<id>",
      segment: "<value>",
      language: "<value>",
      where: "<value>",
      queries: [
        "<value 1>",
        "<value 2>",
        "<value 3>",
      ],
    },
  ],
  next: "<value>",
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `planId`                                                                             | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `version`                                                                            | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `ready`                                                                              | *false*                                                                              | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `assumptions`                                                                        | [operations.Assumption1](../../models/operations/assumption1.md)[]                   | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `questions`                                                                          | [operations.Question1](../../models/operations/question1.md)[]                       | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `segments`                                                                           | [operations.Segment1](../../models/operations/segment1.md)[]                         | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `searches`                                                                           | [operations.PlanSearchesSearch1](../../models/operations/plan-searches-search1.md)[] | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `unread`                                                                             | [operations.Unread1](../../models/operations/unread1.md)[]                           | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `next`                                                                               | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |