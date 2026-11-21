# SearchCompaniesItem

## Example Usage

```typescript
import { SearchCompaniesItem } from "bereach/models/operations";

let value: SearchCompaniesItem = {
  type: "COMPANY",
  name: "<value>",
  profileUrl: "https://austere-challenge.info",
  summary: "<value>",
  industry: "<value>",
  location: "<value>",
  followersCount: 770990,
  website: "<value>",
  employees: 412874,
  foundedYear: 863803,
};
```

## Fields

| Field                                                                                                                 | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                                | [operations.SearchCompaniesType](../../models/operations/search-companies-type.md)                                    | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `name`                                                                                                                | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `profileUrl`                                                                                                          | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | The company's LinkedIn page, when the provider names it; null otherwise (pass `name` to publicCompany to resolve it). |
| `summary`                                                                                                             | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `industry`                                                                                                            | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `location`                                                                                                            | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | N/A                                                                                                                   |
| `followersCount`                                                                                                      | *number*                                                                                                              | :heavy_check_mark:                                                                                                    | Followers, on a company looked up by its name; null on a search, whose provider does not count them.                  |
| `logoUrl`                                                                                                             | *string*                                                                                                              | :heavy_minus_sign:                                                                                                    | The company's logo, when the provider has one.                                                                        |
| `website`                                                                                                             | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | The company's own homepage.                                                                                           |
| `employees`                                                                                                           | *number*                                                                                                              | :heavy_check_mark:                                                                                                    | Headcount, when the provider records it.                                                                              |
| `foundedYear`                                                                                                         | *number*                                                                                                              | :heavy_check_mark:                                                                                                    | The year the company was founded, when the provider records it.                                                       |