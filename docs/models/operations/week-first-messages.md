# WeekFirstMessages

## Example Usage

```typescript
import { WeekFirstMessages } from "bereach/models/operations";

let value: WeekFirstMessages = {
  sent: 933302,
  won: 365136,
  rate: 61781,
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `sent`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `won`                                                                                 | *number*                                                                              | :heavy_check_mark:                                                                    | Accepted (an invitation) or answered (a first message) within withinDays of going out |
| `rate`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | Whole percent; null under ten sent                                                    |