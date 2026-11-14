# ReviewDraftsLine

What the line did with the approved first messages. Null when nothing was approved.

## Example Usage

```typescript
import { ReviewDraftsLine } from "bereach/models/operations";

let value: ReviewDraftsLine = {
  queued: 132760,
  requeued: 928838,
  alreadyQueued: 901501,
  held: 198394,
  skipped: [],
  invitesQueued: 23110,
  accounts: [],
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `queued`                                                                             | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `requeued`                                                                           | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `alreadyQueued`                                                                      | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `held`                                                                               | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `skipped`                                                                            | [operations.ReviewDraftsSkipped](../../models/operations/review-drafts-skipped.md)[] | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `invitesQueued`                                                                      | *number*                                                                             | :heavy_check_mark:                                                                   | Invitations put in line so these messages can follow; not in invitationsApproved.    |
| `accounts`                                                                           | *string*[]                                                                           | :heavy_check_mark:                                                                   | N/A                                                                                  |