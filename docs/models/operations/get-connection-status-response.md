# GetConnectionStatusResponse

Current state of the connection-request lane

## Example Usage

```typescript
import { GetConnectionStatusResponse } from "bereach/models/operations";

let value: GetConnectionStatusResponse = {
  success: true,
  accounts: [],
  totals: {
    waitingTotal: 152562,
    awaitingResponse: 606106,
    sentLast24h: 180372,
    acceptedLast24h: 672000,
    expectedNext24h: 783378,
    expectedIsPartial: true,
    oldestWaitingHours: 560369,
    accountsSending: 208135,
    accountsWaitingForWindow: 46185,
    accountsBlocked: 968776,
    accountsUnreadable: 108399,
    next: {
      contactId: "<id>",
      name: "<value>",
      avatarUrl: "https://worthy-obedience.biz/",
      headline: "<value>",
      linkedinUrl: "https://prestigious-challenge.net/",
      lastActivityAt: "<value>",
      thinProfile: false,
      why: {
        status: "window",
        detail: "<value>",
        clearsItself: true,
        fixUrl: "https://heavy-eggplant.net/",
        kind: "<value>",
        opensAt: "<value>",
      },
      position: 302793,
      sendsAt: "<value>",
      accountLabel: "<value>",
    },
  },
  creditsUsed: 124958,
  retryAfter: 837493,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `accounts`                                                                                                                           | [operations.GetConnectionStatusAccount](../../models/operations/get-connection-status-account.md)[]                                  | :heavy_check_mark:                                                                                                                   | One entry per connected LinkedIn account, each read on its own.                                                                      |
| `totals`                                                                                                                             | [operations.GetConnectionStatusTotals](../../models/operations/get-connection-status-totals.md)                                      | :heavy_check_mark:                                                                                                                   | Everything summed. Null when no account is connected.                                                                                |
| `trend`                                                                                                                              | [operations.Trend](../../models/operations/trend.md)                                                                                 | :heavy_minus_sign:                                                                                                                   | Only when asked with trend true: every account together, day by day and week by week.                                                |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.GetConnectionStatusSpent](../../models/operations/get-connection-status-spent.md)                                        | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |