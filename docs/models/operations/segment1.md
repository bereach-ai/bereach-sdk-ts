# Segment1

## Example Usage

```typescript
import { Segment1 } from "bereach/models/operations";

let value: Segment1 = {
  id: "<id>",
  name: "<value>",
  confidence: "medium",
  kinds: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  places: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  groups: [],
  evidence: [
    {
      source: "<value>",
      quote: "<value>",
    },
  ],
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `id`                                                             | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |
| `name`                                                           | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |
| `confidence`                                                     | [operations.Confidence1](../../models/operations/confidence1.md) | :heavy_check_mark:                                               | N/A                                                              |
| `kinds`                                                          | *string*[]                                                       | :heavy_check_mark:                                               | N/A                                                              |
| `everyIndustry`                                                  | *true*                                                           | :heavy_minus_sign:                                               | N/A                                                              |
| `exampleKind`                                                    | *string*                                                         | :heavy_minus_sign:                                               | N/A                                                              |
| `places`                                                         | *string*[]                                                       | :heavy_check_mark:                                               | N/A                                                              |
| `groups`                                                         | [operations.Group1](../../models/operations/group1.md)[]         | :heavy_check_mark:                                               | N/A                                                              |
| `evidence`                                                       | [operations.Evidence1](../../models/operations/evidence1.md)[]   | :heavy_check_mark:                                               | N/A                                                              |
| `offered`                                                        | [operations.Offered1](../../models/operations/offered1.md)       | :heavy_minus_sign:                                               | N/A                                                              |