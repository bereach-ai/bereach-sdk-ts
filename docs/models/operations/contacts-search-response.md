# ContactsSearchResponse

Matching contacts. The row shape depends on `omitData`.

## Example Usage

```typescript
import { ContactsSearchResponse } from "bereach/models/operations";

let value: ContactsSearchResponse = {
  success: true,
  contacts: [
    {
      id: "<id>",
      linkedinUrl: "https://snoopy-loyalty.com/",
      profileUrn: "<value>",
      publicIdentifier: "<value>",
      name: "<value>",
      lifecycleStage: "<value>",
      notes: "<value>",
      stageChangedAt: null,
      profileUpdatedAt: "<value>",
      conversationUpdatedAt: null,
      tags: [
        "<value 1>",
        "<value 2>",
        "<value 3>",
      ],
      createdAt: "1725511710867",
      updatedAt: "1735611305614",
    },
  ],
  pagination: {
    limit: 76315,
    offset: 229444,
    total: 690471,
  },
  creditsUsed: 162093,
  retryAfter: 969474,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `contacts`                                                                                                                           | *operations.ContactsUnion*                                                                                                           | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `pagination`                                                                                                                         | [operations.ContactsSearchPagination](../../models/operations/contacts-search-pagination.md)                                         | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsSearchSpent](../../models/operations/contacts-search-spent.md)                                                   | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |