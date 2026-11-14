# ListSentInvitationsInvitation

## Example Usage

```typescript
import { ListSentInvitationsInvitation } from "bereach/models/operations";

let value: ListSentInvitationsInvitation = {
  invitationId: "<id>",
  invitationUrn: "<value>",
  entityUrn: "<value>",
  sentAt: "<value>",
  sentTime: 526910,
  message: "<value>",
  targetProfileId: "<id>",
  targetFirstName: "<value>",
  targetLastName: null,
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
  unseen: false,
  inviterFollowingInvitee: false,
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `invitationId`                                              | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `invitationUrn`                                             | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `entityUrn`                                                 | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `sentAt`                                                    | *string*                                                    | :heavy_check_mark:                                          | When the invitation was sent (ISO 8601), read off its id    |
| `sentTime`                                                  | *number*                                                    | :heavy_check_mark:                                          | The same moment in epoch milliseconds                       |
| `message`                                                   | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `targetProfileId`                                           | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `targetFirstName`                                           | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `targetLastName`                                            | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `toMember`                                                  | [operations.ToMember](../../models/operations/to-member.md) | :heavy_check_mark:                                          | N/A                                                         |
| `invitationType`                                            | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `mailboxItemId`                                             | *string*                                                    | :heavy_check_mark:                                          | N/A                                                         |
| `customMessage`                                             | *boolean*                                                   | :heavy_check_mark:                                          | N/A                                                         |
| `unseen`                                                    | *boolean*                                                   | :heavy_check_mark:                                          | N/A                                                         |
| `mutualCurrentCompany`                                      | *any*                                                       | :heavy_minus_sign:                                          | N/A                                                         |
| `connectionDistance`                                        | *any*                                                       | :heavy_minus_sign:                                          | N/A                                                         |
| `inviterFollowingInvitee`                                   | *boolean*                                                   | :heavy_check_mark:                                          | N/A                                                         |