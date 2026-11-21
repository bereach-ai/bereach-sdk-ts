# GetConnectionStatusSendingHours

When this account sends, to answer the user only when they ask about timing. Times are local to timeZone; nextOpensAt is UTC, converted with utcOffset. The user can move the zone, the start of connection requests and the message hours.

## Example Usage

```typescript
import { GetConnectionStatusSendingHours } from "bereach/models/operations";

let value: GetConnectionStatusSendingHours = {
  timeZone: "Asia/Kuwait",
  source: "account",
  utcOffset: "<value>",
  invitations: {
    from: "<value>",
    to: "<value>",
    days: "every day",
    nextOpensAt: "<value>",
  },
  messages: {
    timeZone: "America/Belem",
    from: "<value>",
    to: "<value>",
    days: [],
    nextOpensAt: "<value>",
  },
};
```

## Fields

| Field                                                                                                                                                                      | Type                                                                                                                                                                       | Required                                                                                                                                                                   | Description                                                                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `timeZone`                                                                                                                                                                 | *string*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                         | The zone the hours below follow, an IANA zone name.                                                                                                                        |
| `source`                                                                                                                                                                   | [operations.GetConnectionStatusSource](../../models/operations/get-connection-status-source.md)                                                                            | :heavy_check_mark:                                                                                                                                                         | Where the zone came from. setting: the user set it. none: nothing placed them, so the hours run on UTC. Any other value is an automatic guess, which the user can correct. |
| `utcOffset`                                                                                                                                                                | *string*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                         | The zone's offset from UTC right now, such as +02:00. Use it to convert every time here to the user's own clock.                                                           |
| `invitations`                                                                                                                                                              | [operations.AccountInvitations](../../models/operations/account-invitations.md)                                                                                            | :heavy_check_mark:                                                                                                                                                         | N/A                                                                                                                                                                        |
| `messages`                                                                                                                                                                 | [operations.GetConnectionStatusMessages](../../models/operations/get-connection-status-messages.md)                                                                        | :heavy_check_mark:                                                                                                                                                         | N/A                                                                                                                                                                        |