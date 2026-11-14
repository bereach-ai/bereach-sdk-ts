# ContactsGetByUrlResponse

Contact found

## Example Usage

```typescript
import { ContactsGetByUrlResponse } from "bereach/models/operations";

let value: ContactsGetByUrlResponse = {
  success: true,
  contact: {
    id: "<id>",
    linkedinUrl: "https://scented-turret.com",
    profileUrn: "<value>",
    publicIdentifier: "<value>",
    name: "<value>",
    lifecycleStage: "<value>",
    notes: "<value>",
    stageChangedAt: "<value>",
    profileUpdatedAt: "<value>",
    conversationUpdatedAt: null,
    campaigns: [
      {
        campaignId: "<id>",
        campaignName: "<value>",
        source: "<value>",
        sourceAngle: "<value>",
        addedAt: "<value>",
      },
    ],
    tags: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
    createdAt: "1709212674258",
    updatedAt: "1735633614722",
  },
  creditsUsed: 588027,
  retryAfter: 747349,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `contact`                                                                                                                            | [operations.ContactsGetByUrlContact](../../models/operations/contacts-get-by-url-contact.md)                                         | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsGetByUrlSpent](../../models/operations/contacts-get-by-url-spent.md)                                             | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |