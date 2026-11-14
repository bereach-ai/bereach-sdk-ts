# Public2

## Example Usage

```typescript
import { Public2 } from "bereach/models/operations";

let value: Public2 = {
  source: "public",
  creditsUsed: 484616,
  saved: 392787,
  found: 176587,
  notFound: 277290,
  unreadable: 292655,
  profiles: [
    {
      asked: "<value>",
      outcome: "not_found",
    },
  ],
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `source`                                                                                                                             | [operations.PublicProfileSource2](../../models/operations/public-profile-source2.md)                                                 | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `creditsUsed`                                                                                                                        | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | Credits this call spent, net of anything given back, for code: tell the user `spent`, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                              | [operations.PublicProfileSpent2](../../models/operations/public-profile-spent2.md)                                                   | :heavy_minus_sign:                                                                                                                   | What this call spent, in money: the figure to tell the user, written as text says it.                                                |
| `saved`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | How many people were saved to your contacts.                                                                                         |
| `found`                                                                                                                              | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | How many distinct people were found.                                                                                                 |
| `notFound`                                                                                                                           | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `unreadable`                                                                                                                         | *number*                                                                                                                             | :heavy_check_mark:                                                                                                                   | N/A                                                                                                                                  |
| `profiles`                                                                                                                           | [operations.PublicProfileProfile](../../models/operations/public-profile-profile.md)[]                                               | :heavy_check_mark:                                                                                                                   | One row per address asked, in the order asked.                                                                                       |
| `employerNote`                                                                                                                       | *string*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | What the employer facts on the rows came to.                                                                                         |