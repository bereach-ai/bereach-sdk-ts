# ContactsUpsertResponse

Contacts created or updated

## Example Usage

```typescript
import { ContactsUpsertResponse } from "bereach/models/operations";

let value: ContactsUpsertResponse = {
  success: true,
  results: {
    created: 80370,
    updated: 158766,
    skipped: 398554,
    errors: [],
  },
  contacts: [],
  creditsUsed: 501987,
  retryAfter: 579520,
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `success`                                                                                                                            | *true*                                                                                                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `results`                                                                                                                            | [operations.ContactsUpsertResults](../../models/operations/contacts-upsert-results.md)                                               | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `contacts`                                                                                                                           | [operations.ContactsUpsertContactResponseBody](../../models/operations/contacts-upsert-contact-response-body.md)[]                   | :heavy_check_mark:                                                                                                                   | The rows as written. No per-campaign fields: this route creates no campaign membership.                                              |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.ContactsUpsertSpent](../../models/operations/contacts-upsert-spent.md)                                                   | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `retryAfter`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                     |