# SearchParametersItem

## Example Usage

```typescript
import { SearchParametersItem } from "bereach/models/operations";

let value: SearchParametersItem = {
  id: "<id>",
  title: "<value>",
  type: "<value>",
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `id`                                                                                     | *string*                                                                                 | :heavy_check_mark:                                                                       | The id LinkedIn's own filters take.                                                      |
| `title`                                                                                  | *string*                                                                                 | :heavy_check_mark:                                                                       | Human-readable label for the id.                                                         |
| `type`                                                                                   | *string*                                                                                 | :heavy_check_mark:                                                                       | Echo of the requested type.                                                              |
| `displayValue`                                                                           | *string*                                                                                 | :heavy_minus_sign:                                                                       | Present on the closed-enum types.                                                        |
| `source`                                                                                 | *string*                                                                                 | :heavy_minus_sign:                                                                       | Where the id came from: a lookup, our alias list, or the Sales Navigator list of values. |
| `aliasKind`                                                                              | *string*                                                                                 | :heavy_minus_sign:                                                                       | Present when the curated alias map answered.                                             |