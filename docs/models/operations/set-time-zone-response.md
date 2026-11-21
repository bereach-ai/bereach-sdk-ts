# SetTimeZoneResponse

The zone and hours are saved

## Example Usage

```typescript
import { SetTimeZoneResponse } from "bereach/models/operations";

let value: SetTimeZoneResponse = {
  success: true,
  sendingHours: {
    timeZone: "Asia/Macau",
    source: "setting",
    utcOffset: "<value>",
    invitations: {
      from: "<value>",
      to: "<value>",
      days: "every day",
      nextOpensAt: "<value>",
    },
    messages: {
      timeZone: "Africa/Djibouti",
      from: "<value>",
      to: "<value>",
      days: [
        "<value 1>",
      ],
      nextOpensAt: "<value>",
    },
  },
  creditsUsed: 241247,
  retryAfter: 918655,
};
```

## Fields

| Field                                                                                                                                                                                                                                       | Type                                                                                                                                                                                                                                        | Required                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                                                                                                                   | *true*                                                                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                                                          | N/A                                                                                                                                                                                                                                         |
| `sendingHours`                                                                                                                                                                                                                              | [operations.SetTimeZoneSendingHours](../../models/operations/set-time-zone-sending-hours.md)                                                                                                                                                | :heavy_check_mark:                                                                                                                                                                                                                          | When this account sends, to answer the user only when they ask about timing. Times are local to timeZone; nextOpensAt is UTC, converted with utcOffset. The user can move the zone, the start of connection requests and the message hours. |
| `creditsUsed`                                                                                                                                                                                                                               | *number*                                                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                                                          | Credits this call spent, net of anything given back, for code. 0 when nothing was charged.                                                                                                                                                  |
| `spent`                                                                                                                                                                                                                                     | [operations.SetTimeZoneSpent](../../models/operations/set-time-zone-spent.md)                                                                                                                                                               | :heavy_minus_sign:                                                                                                                                                                                                                          | What this call spent, in money.                                                                                                                                                                                                             |
| `retryAfter`                                                                                                                                                                                                                                | *number*                                                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                                                          | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                                                                                                                            |