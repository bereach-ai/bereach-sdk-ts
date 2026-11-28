# WeekInvitations

## Example Usage

```typescript
import { WeekInvitations } from "bereach/models/operations";

let value: WeekInvitations = {
  sent: 18892,
  won: 265166,
  rate: 802297,
  withNote: {
    sent: 980177,
    won: 879935,
    rate: 434505,
  },
  withoutNote: {
    sent: 802418,
    won: 805254,
    rate: 225083,
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `sent`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `won`                                                                                 | *number*                                                                              | :heavy_check_mark:                                                                    | Accepted (an invitation) or answered (a first message) within withinDays of going out |
| `rate`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | Whole percent; null under ten sent                                                    |
| `withNote`                                                                            | [operations.WeekWithNote](../../models/operations/week-with-note.md)                  | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `withoutNote`                                                                         | [operations.WeekWithoutNote](../../models/operations/week-without-note.md)            | :heavy_check_mark:                                                                    | N/A                                                                                   |