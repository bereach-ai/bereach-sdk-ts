# ContactsBriefCompany

## Example Usage

```typescript
import { ContactsBriefCompany } from "bereach/models/operations";

let value: ContactsBriefCompany = {
  found: false,
  card: {
    readAt: "<value>",
    name: "<value>",
    slug: "<value>",
    url: "https://strict-linseed.biz",
    tagline: "<value>",
    description: "edge meh litter deceivingly whirlwind since",
    website: "<value>",
    industry: "<value>",
    founded: 7040.92,
    employees: 3517.73,
    followers: 4710.7,
    location: "<value>",
    recentPosts: [],
  },
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `found`                                                                    | *boolean*                                                                  | :heavy_check_mark:                                                         | N/A                                                                        |
| `reason`                                                                   | [operations.CompanyReason](../../models/operations/company-reason.md)      | :heavy_minus_sign:                                                         | Why this part is empty or older than asked.                                |
| `readFrom`                                                                 | [operations.CompanyReadFrom](../../models/operations/company-read-from.md) | :heavy_minus_sign:                                                         | N/A                                                                        |
| `readAt`                                                                   | *string*                                                                   | :heavy_minus_sign:                                                         | When what this part shows was read.                                        |
| `card`                                                                     | [operations.Card](../../models/operations/card.md)                         | :heavy_check_mark:                                                         | N/A                                                                        |