# PlanSearchesResponseBody3

## Example Usage

```typescript
import { PlanSearchesResponseBody3 } from "bereach/models/operations";

let value: PlanSearchesResponseBody3 = {
  reason: "<value>",
  searches: [
    {
      id: "<id>",
      segment: "<value>",
      language: "<value>",
      where: "<value>",
      queries: [
        "<value 1>",
      ],
    },
  ],
  next: "<value>",
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `reason`                                                                             | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `searches`                                                                           | [operations.PlanSearchesSearch3](../../models/operations/plan-searches-search3.md)[] | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `unread`                                                                             | [operations.Unread3](../../models/operations/unread3.md)[]                           | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `next`                                                                               | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |