# AxesTried

## Example Usage

```typescript
import { AxesTried } from "bereach/models/operations";

let value: AxesTried = {
  axis: "<value>",
  queries: 156145,
  found: 725063,
  fresh: 130260,
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `axis`                                                                 | *string*                                                               | :heavy_check_mark:                                                     | Which angle this row covers.                                           |
| `queries`                                                              | *number*                                                               | :heavy_check_mark:                                                     | How many searches this angle actually ran.                             |
| `found`                                                                | *number*                                                               | :heavy_check_mark:                                                     | Everybody those searches returned, before duplicates were removed.     |
| `fresh`                                                                | *number*                                                               | :heavy_check_mark:                                                     | People this angle contributed that no earlier angle had already named. |