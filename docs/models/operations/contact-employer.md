# ContactEmployer

The person's current employer, from that company's own record, when one was read for them.

## Example Usage

```typescript
import { ContactEmployer } from "bereach/models/operations";

let value: ContactEmployer = {
  name: "<value>",
  employees: 1737.59,
  industry: "<value>",
  hq: {
    city: null,
    postcode: "06998-9737",
    country: "Serbia",
  },
  linkedinUrl: "https://defensive-promise.biz/",
  website: null,
  readAt: "<value>",
};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `name`                                                        | *string*                                                      | :heavy_check_mark:                                            | N/A                                                           |
| `employees`                                                   | *number*                                                      | :heavy_check_mark:                                            | How many people the company employs, by its own record.       |
| `industry`                                                    | *string*                                                      | :heavy_check_mark:                                            | What kind of company it is, by its own record.                |
| `hq`                                                          | [operations.ContactHq](../../models/operations/contact-hq.md) | :heavy_check_mark:                                            | Where its headquarters are.                                   |
| `founded`                                                     | *number*                                                      | :heavy_minus_sign:                                            | The year it was founded.                                      |
| `linkedinUrl`                                                 | *string*                                                      | :heavy_check_mark:                                            | The company's own page, when known.                           |
| `website`                                                     | *string*                                                      | :heavy_check_mark:                                            | N/A                                                           |
| `readAt`                                                      | *string*                                                      | :heavy_check_mark:                                            | N/A                                                           |