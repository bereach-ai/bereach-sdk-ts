# FundingFilter

What the funding window did, present whenever the ask carried one.

## Example Usage

```typescript
import { FundingFilter } from "bereach/models/operations";

let value: FundingFilter = {
  months: 3392.74,
  kept: 6250.5,
  outside: 2583.23,
  unknown: 2646.85,
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `months`                                                        | *number*                                                        | :heavy_check_mark:                                              | The window asked, in months.                                    |
| `kept`                                                          | *number*                                                        | :heavy_check_mark:                                              | Companies on this page whose latest round is inside the window. |
| `outside`                                                       | *number*                                                        | :heavy_check_mark:                                              | Companies left out because their latest round is older.         |
| `unknown`                                                       | *number*                                                        | :heavy_check_mark:                                              | Companies left out because no dated round is recorded for them. |