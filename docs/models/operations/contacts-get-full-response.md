# ContactsGetFullResponse

Contact details

## Example Usage

```typescript
import { ContactsGetFullResponse } from "bereach/models/operations";

let value: ContactsGetFullResponse = {
  success: true,
  contact: {
    id: "<id>",
    linkedinUrl: "https://livid-atrium.name/",
    profileUrn: "<value>",
    publicIdentifier: "<value>",
    name: "<value>",
    lifecycleStage: "<value>",
    notes: "<value>",
    stageChangedAt: "<value>",
    profileUpdatedAt: "<value>",
    conversationUpdatedAt: "<value>",
    campaigns: [],
    tags: [],
    createdAt: "1733507176243",
    updatedAt: "1735621071156",
  },
  creditsUsed: 357832,
  retryAfter: 576705,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `contact`                                                                                                                            | [operations.ContactsGetFullContact](../../models/operations/contacts-get-full-contact.md)                                            | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsGetFullSpent](../../models/operations/contacts-get-full-spent.md)                                                | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |