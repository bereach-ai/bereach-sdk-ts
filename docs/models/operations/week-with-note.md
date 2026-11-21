# WeekWithNote

## Example Usage

```typescript
import { WeekWithNote } from "bereach/models/operations";

let value: WeekWithNote = {
  sent: 772070,
  won: 255464,
  rate: 994899,
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `sent`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `won`                                                                                 | *number*                                                                              | :heavy_check_mark:                                                                    | Accepted (an invitation) or answered (a first message) within withinDays of going out |
| `rate`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | Whole percent; null under ten sent                                                    |