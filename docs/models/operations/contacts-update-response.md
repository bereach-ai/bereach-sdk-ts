# ContactsUpdateResponse

Updated contact

## Example Usage

```typescript
import { ContactsUpdateResponse } from "bereach/models/operations";

let value: ContactsUpdateResponse = {
  success: true,
  contact: {
    id: "<id>",
    linkedinUrl: "https://agreeable-siege.net/",
    profileUrn: "<value>",
    publicIdentifier: "<value>",
    name: "<value>",
    lifecycleStage: "<value>",
    notes: "<value>",
    stageChangedAt: "<value>",
    profileUpdatedAt: null,
    conversationUpdatedAt: "<value>",
    tags: [],
    createdAt: "1730976024066",
    updatedAt: "1735635644299",
  },
  creditsUsed: 226824,
  retryAfter: 757269,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `contact`                                                                                                                            | [operations.ContactsUpdateContact](../../models/operations/contacts-update-contact.md)                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsUpdateSpent](../../models/operations/contacts-update-spent.md)                                                   | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |