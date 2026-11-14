# PublicFindCompaniesSizeFilter

What the company-size band did, present whenever the ask carried one.

## Example Usage

```typescript
import { PublicFindCompaniesSizeFilter } from "bereach/models/operations";

let value: PublicFindCompaniesSizeFilter = {
  min: 9503.17,
  max: 796.75,
  kept: 6230.5,
  outOfBand: 8024.03,
  sizeUnknown: 8980.39,
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `min`                                                           | *number*                                                        | :heavy_check_mark:                                              | The smallest company size asked, or null.                       |
| `max`                                                           | *number*                                                        | :heavy_check_mark:                                              | The largest company size asked, or null.                        |
| `kept`                                                          | *number*                                                        | :heavy_check_mark:                                              | Companies on this page inside the size.                         |
| `outOfBand`                                                     | *number*                                                        | :heavy_check_mark:                                              | Companies left out because their headcount is outside the size. |
| `sizeUnknown`                                                   | *number*                                                        | :heavy_check_mark:                                              | Companies left out because they state no headcount.             |