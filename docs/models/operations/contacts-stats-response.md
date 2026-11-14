# ContactsStatsResponse

Contact statistics

## Example Usage

```typescript
import { ContactsStatsResponse } from "bereach/models/operations";

let value: ContactsStatsResponse = {
  success: true,
  funnel: {
    contact: 384874,
    lead: 875424,
    qualified: 451462,
    rejected: 127820,
  },
  foundPeople: 687032,
  bySource: {
    "key": 444,
  },
  bySourceAngle: {
    "key": {
      total: 215492,
      contact: 943075,
      lead: 491122,
      qualified: 912365,
      rejected: 467067,
    },
  },
  byCampaign: {},
  daily: [],
  creditsUsed: 162543,
  retryAfter: 80979,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `funnel`                                                                                                                             | [operations.Funnel](../../models/operations/funnel.md)                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `foundPeople`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Everyone found, each person counted once, not counting removed. The funnel counts a person once per list they are on.                |
| `bySource`                                                                                                                           | Record<string, *number*>                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `bySourceAngle`                                                                                                                      | Record<string, [operations.BySourceAngle](../../models/operations/by-source-angle.md)>                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `byCampaign`                                                                                                                         | Record<string, [operations.ByCampaign](../../models/operations/by-campaign.md)>                                                      | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `daily`                                                                                                                              | [operations.ContactsStatsDaily](../../models/operations/contacts-stats-daily.md)[]                                                   | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsStatsSpent](../../models/operations/contacts-stats-spent.md)                                                     | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |