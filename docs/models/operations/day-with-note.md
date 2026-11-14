# DayWithNote

## Example Usage

```typescript
import { DayWithNote } from "bereach/models/operations";

let value: DayWithNote = {
  sent: 682554,
  won: 873086,
  rate: 978369,
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `sent`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `won`                                                                                 | *number*                                                                              | :heavy_check_mark:                                                                    | Accepted (an invitation) or answered (a first message) within withinDays of going out |
| `rate`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | Whole percent; null under ten sent                                                    |