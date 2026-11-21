# SetTimeZoneMessages

## Example Usage

```typescript
import { SetTimeZoneMessages } from "bereach/models/operations";

let value: SetTimeZoneMessages = {
  timeZone: "Africa/Bangui",
  from: "<value>",
  to: "<value>",
  days: [],
  nextOpensAt: "<value>",
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `timeZone`                                                      | *string*                                                        | :heavy_check_mark:                                              | The zone these hours follow, the same as timeZone.              |
| `from`                                                          | *string*                                                        | :heavy_check_mark:                                              | When first messages start, local time.                          |
| `to`                                                            | *string*                                                        | :heavy_check_mark:                                              | When they stop, local time; 24:00 is midnight.                  |
| `days`                                                          | *string*[]                                                      | :heavy_check_mark:                                              | The weekdays first messages go out on.                          |
| `nextOpensAt`                                                   | *string*                                                        | :heavy_check_mark:                                              | When the hours next open, in UTC. Null while they are open now. |