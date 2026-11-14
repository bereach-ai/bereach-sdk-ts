# ReviewDraftsResponse

Review applied

## Example Usage

```typescript
import { ReviewDraftsResponse } from "bereach/models/operations";

let value: ReviewDraftsResponse = {
  success: true,
  approved: 701863,
  rejected: 175028,
  ineligible: {
    approved: [
      {
        id: "<id>",
        currentStatus: "<value>",
      },
    ],
    rejected: [
      {
        id: "<id>",
        currentStatus: null,
      },
    ],
  },
  invitationsApproved: 71942,
  line: {
    queued: 139292,
    requeued: 548203,
    alreadyQueued: 248534,
    held: 183934,
    skipped: [],
    invitesQueued: 157312,
    accounts: [],
  },
  laneBlocked: [],
  creditsUsed: 575063,
  retryAfter: 419632,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `approved`                                                                                                                           | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Rows now in line: first messages queued, put back or already there, plus connection requests approved.                               |
| `rejected`                                                                                                                           | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `ineligible`                                                                                                                         | [operations.ReviewDraftsIneligible](../../models/operations/review-drafts-ineligible.md)                                             | :heavy_check_mark:                                                                                                                   | Ids that were not in draft, with the status they were in.                                                                            |
| `invitationsApproved`                                                                                                                | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Connection requests among the approved ids, handed to the invitation line.                                                           |
| `line`                                                                                                                               | [operations.ReviewDraftsLine](../../models/operations/review-drafts-line.md)                                                         | :heavy_check_mark:                                                                                                                   | What the line did with the approved first messages. Null when nothing was approved.                                                  |
| `laneBlocked`                                                                                                                        | [operations.LaneBlocked](../../models/operations/lane-blocked.md)[]                                                                  | :heavy_check_mark:                                                                                                                   | Rows not approved because their lane is switched off for the list.                                                                   |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ReviewDraftsSpent](../../models/operations/review-drafts-spent.md)                                                       | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |