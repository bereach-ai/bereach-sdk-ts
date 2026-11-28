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
  line: null,
  creditsUsed: 615294,
  retryAfter: 139292,
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `success`                                                                                  | *true*                                                                                     | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `approved`                                                                                 | *number*                                                                                   | :heavy_check_mark:                                                                         | First messages now in line: queued, put back or already there.                             |
| `rejected`                                                                                 | *number*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `ineligible`                                                                               | [operations.ReviewDraftsIneligible](../../models/operations/review-drafts-ineligible.md)   | :heavy_check_mark:                                                                         | Ids that were not in draft, with the status they were in.                                  |
| `line`                                                                                     | [operations.ReviewDraftsLine](../../models/operations/review-drafts-line.md)               | :heavy_check_mark:                                                                         | What the line did with the approved first messages. Null when nothing was approved.        |
| `creditsUsed`                                                                              | *number*                                                                                   | :heavy_check_mark:                                                                         | Credits this call spent, net of anything given back, for code. 0 when nothing was charged. |
| `spent`                                                                                    | [operations.ReviewDraftsSpent](../../models/operations/review-drafts-spent.md)             | :heavy_minus_sign:                                                                         | What this call spent, in money.                                                            |
| `retryAfter`                                                                               | *number*                                                                                   | :heavy_check_mark:                                                                         | Seconds to wait before another call of the same type. 0 means no wait is needed.           |