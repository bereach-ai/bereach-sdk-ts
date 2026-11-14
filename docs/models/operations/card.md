# Card

## Example Usage

```typescript
import { Card } from "bereach/models/operations";

let value: Card = {
  readAt: "<value>",
  name: "<value>",
  slug: "<value>",
  url: "https://french-sauerkraut.net",
  tagline: "<value>",
  description: "jury and spiteful hyphenation taxicab bashfully satisfy",
  website: "<value>",
  industry: "<value>",
  founded: 8223.35,
  employees: 7389.35,
  followers: 5264.38,
  location: "<value>",
  recentPosts: [
    {
      text: "<value>",
      url: "https://foolish-assist.com/",
      at: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `readAt`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `slug`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `url`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `tagline`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `website`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `industry`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `founded`                                                                                     | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `employees`                                                                                   | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `followers`                                                                                   | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `location`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `recentPosts`                                                                                 | [operations.ContactsBriefRecentPost](../../models/operations/contacts-brief-recent-post.md)[] | :heavy_check_mark:                                                                            | N/A                                                                                           |