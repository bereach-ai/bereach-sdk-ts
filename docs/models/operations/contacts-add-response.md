# ContactsAddResponse

Contacts added

## Example Usage

```typescript
import { ContactsAddResponse } from "bereach/models/operations";

let value: ContactsAddResponse = {
  success: true,
  results: {
    created: 213604,
    skipped: 355382,
    errors: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
  },
  creditsUsed: 159936,
  retryAfter: 171957,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `results`                                                                                                                            | [operations.ContactsAddResults](../../models/operations/contacts-add-results.md)                                                     | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsAddSpent](../../models/operations/contacts-add-spent.md)                                                         | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |