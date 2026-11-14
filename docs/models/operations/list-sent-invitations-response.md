# ListSentInvitationsResponse

Sent invitations

## Example Usage

```typescript
import { ListSentInvitationsResponse } from "bereach/models/operations";

let value: ListSentInvitationsResponse = {
  success: true,
  invitations: [
    {
      invitationId: "<id>",
      invitationUrn: "<value>",
      entityUrn: "<value>",
      sentAt: "<value>",
      sentTime: 328835,
      message: "<value>",
      targetProfileId: "<id>",
      targetFirstName: "<value>",
      targetLastName: "<value>",
      toMember: {
        name: "<value>",
        headline: "<value>",
        profileUrl: "https://kaleidoscopic-deck.net",
        profilePicture: "<value>",
        publicIdentifier: "<value>",
        profileUrn: "<value>",
        memberId: "<id>",
      },
      invitationType: "<value>",
      mailboxItemId: "<id>",
      customMessage: true,
      unseen: true,
      inviterFollowingInvitee: true,
    },
  ],
  total: 95899,
  start: 235331,
  count: 644397,
  creditsUsed: 265127,
  retryAfter: 774772,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `invitations`                                                                                                                        | [operations.ListSentInvitationsInvitation](../../models/operations/list-sent-invitations-invitation.md)[]                            | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `total`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `start`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `count`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `olderThanDays`                                                                                                                      | *number*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | The olderThanDays this answer was read with, echoed                                                                                  |
| `scanFrom`                                                                                                                           | *number*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | The scanFrom this answer read from, echoed                                                                                           |
| `totalIsExact`                                                                                                                       | *false*                                                                                                                              | :heavy_minus_sign:                                                                                                                   | Present when total counts only the part of the list this answer read                                                                 |
| `hasMore`                                                                                                                            | *true*                                                                                                                               | :heavy_minus_sign:                                                                                                                   | Present when more invitations follow this answer                                                                                     |
| `nextStart`                                                                                                                          | *number*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | Without olderThanDays: the start of the next page                                                                                    |
| `nextScanFrom`                                                                                                                       | *number*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | With olderThanDays: pass as scanFrom to read the next part of the list                                                               |
| `warning`                                                                                                                            | *string*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | Present ONLY when the list could not be confirmed complete. While it is present, absence from `invitations` proves nothing.          |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ListSentInvitationsSpent](../../models/operations/list-sent-invitations-spent.md)                                        | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |