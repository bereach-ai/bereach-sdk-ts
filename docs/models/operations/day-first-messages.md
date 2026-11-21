# DayFirstMessages

## Example Usage

```typescript
import { DayFirstMessages } from "bereach/models/operations";

let value: DayFirstMessages = {
  sent: 721618,
  won: 441367,
  rate: 139804,
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `sent`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | N/A                                                                                   |
| `won`                                                                                 | *number*                                                                              | :heavy_check_mark:                                                                    | Accepted (an invitation) or answered (a first message) within withinDays of going out |
| `rate`                                                                                | *number*                                                                              | :heavy_check_mark:                                                                    | Whole percent; null under ten sent                                                    |