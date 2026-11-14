# ContactsListResponse

Campaign contacts

## Example Usage

```typescript
import { ContactsListResponse } from "bereach/models/operations";

let value: ContactsListResponse = {
  success: true,
  contacts: [
    {
      id: "<id>",
      linkedinUrl: "https://dependable-fat.name/",
      profileUrn: "<value>",
      publicIdentifier: "<value>",
      name: "<value>",
      lifecycleStage: "<value>",
      notes: "<value>",
      stageChangedAt: "<value>",
      profileUpdatedAt: "<value>",
      conversationUpdatedAt: null,
      tags: [
        "<value 1>",
        "<value 2>",
      ],
      createdAt: "1717712455945",
      updatedAt: "1735673502786",
      source: "<value>",
      sourceAngle: "<value>",
      addedAt: "<value>",
    },
  ],
  pagination: {
    limit: 203707,
    offset: 633082,
    total: 306599,
  },
  creditsUsed: 174437,
  retryAfter: 375309,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `contacts`                                                                                                                           | [operations.ContactsListContact](../../models/operations/contacts-list-contact.md)[]                                                 | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `pagination`                                                                                                                         | [operations.ContactsListPagination](../../models/operations/contacts-list-pagination.md)                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsListSpent](../../models/operations/contacts-list-spent.md)                                                       | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |