# SetTimeZoneSendingHours

When this account sends, to answer the user only when they ask about timing. Times are local to timeZone; nextOpensAt is UTC, converted with utcOffset. The user can move the zone, the start of connection requests and the message hours.

## Example Usage

```typescript
import { SetTimeZoneSendingHours } from "bereach/models/operations";

let value: SetTimeZoneSendingHours = {
  timeZone: "Pacific/Funafuti",
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
};
```

## Fields

| Field                                                                                                                                                                      | Type                                                                                                                                                                       | Required                                                                                                                                                                   | Description                                                                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `timeZone`                                                                                                                                                                 | *string*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                         | The zone the hours below follow, an IANA zone name.                                                                                                                        |
| `source`                                                                                                                                                                   | [operations.SetTimeZoneSource](../../models/operations/set-time-zone-source.md)                                                                                            | :heavy_check_mark:                                                                                                                                                         | Where the zone came from. setting: the user set it. none: nothing placed them, so the hours run on UTC. Any other value is an automatic guess, which the user can correct. |
| `utcOffset`                                                                                                                                                                | *string*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                         | The zone's offset from UTC right now, such as +02:00. Use it to convert every time here to the user's own clock.                                                           |
| `invitations`                                                                                                                                                              | [operations.SetTimeZoneInvitations](../../models/operations/set-time-zone-invitations.md)                                                                                  | :heavy_check_mark:                                                                                                                                                         | N/A                                                                                                                                                                        |
| `messages`                                                                                                                                                                 | [operations.SetTimeZoneMessages](../../models/operations/set-time-zone-messages.md)                                                                                        | :heavy_check_mark:                                                                                                                                                         | N/A                                                                                                                                                                        |