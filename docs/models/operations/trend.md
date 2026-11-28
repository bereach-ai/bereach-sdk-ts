# Trend

Only when asked with trend true: every account together, day by day and week by week.

## Example Usage

```typescript
import { Trend } from "bereach/models/operations";

let value: Trend = {
  withinDays: 686660,
  reading: "<value>",
  weeks: [],
  days: [],
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `withinDays`                                                                                  | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `reading`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | One sentence on how to read the periods                                                       |
| `weeks`                                                                                       | [operations.GetConnectionStatusWeek](../../models/operations/get-connection-status-week.md)[] | :heavy_check_mark:                                                                            | The last six weeks, oldest first                                                              |
| `days`                                                                                        | [operations.GetConnectionStatusDay](../../models/operations/get-connection-status-day.md)[]   | :heavy_check_mark:                                                                            | The last fourteen days, oldest first                                                          |