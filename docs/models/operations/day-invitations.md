# DayInvitations

## Example Usage

```typescript
import { DayInvitations } from "bereach/models/operations";

let value: DayInvitations = {
  sent: 498003,
  won: 315037,
  rate: 758667,
  withNote: {
    sent: 673473,
    won: 717846,
    rate: 876690,
  },
  withoutNote: {
    sent: 730592,
    won: 758126,
    rate: 83839,
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `sent`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `won`                                                                                 | *number*                                                                              | :heavy_check_mark:                                                                    | Accepted (an invitation) or answered (a first message) within withinDays of going out |
| `rate`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | Whole percent; null under ten sent                                                    |
| `withNote`                                                                            | [operations.DayWithNote](../../models/operations/day-with-note.md)                    | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `withoutNote`                                                                         | [operations.DayWithoutNote](../../models/operations/day-without-note.md)              | :heavy_check_mark:                                                                    | N/A                                                                                   |