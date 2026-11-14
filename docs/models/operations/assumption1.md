# Assumption1

## Example Usage

```typescript
import { Assumption1 } from "bereach/models/operations";

let value: Assumption1 = {
  fact: "<value>",
  origin: "inferred",
  source: "<value>",
  use: "search",
  applied: false,
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `fact`                                                   | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `origin`                                                 | [operations.Origin1](../../models/operations/origin1.md) | :heavy_check_mark:                                       | N/A                                                      |
| `source`                                                 | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `use`                                                    | [operations.Use1](../../models/operations/use1.md)       | :heavy_check_mark:                                       | N/A                                                      |
| `applied`                                                | *boolean*                                                | :heavy_check_mark:                                       | Whether this fact acts on the search now.                |