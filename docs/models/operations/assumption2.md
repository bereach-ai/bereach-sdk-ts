# Assumption2

## Example Usage

```typescript
import { Assumption2 } from "bereach/models/operations";

let value: Assumption2 = {
  fact: "<value>",
  origin: "inferred",
  source: "<value>",
  use: "search",
  applied: true,
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `fact`                                                   | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `origin`                                                 | [operations.Origin2](../../models/operations/origin2.md) | :heavy_check_mark:                                       | N/A                                                      |
| `source`                                                 | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `use`                                                    | [operations.Use2](../../models/operations/use2.md)       | :heavy_check_mark:                                       | N/A                                                      |
| `applied`                                                | *boolean*                                                | :heavy_check_mark:                                       | Whether this fact acts on the search now.                |