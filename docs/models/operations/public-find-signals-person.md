# PublicFindSignalsPerson

## Example Usage

```typescript
import { PublicFindSignalsPerson } from "bereach/models/operations";

let value: PublicFindSignalsPerson = {
  name: "<value>",
  headline: "<value>",
  currentTitle: "<value>",
  location: "<value>",
  profileUrl: "https://impish-final.net",
  imageUrl: "https://monumental-mom.name/",
  companyOnProfile: "before",
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `name`                                                                                                    | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `headline`                                                                                                | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `currentTitle`                                                                                            | *string*                                                                                                  | :heavy_check_mark:                                                                                        | Their job at the company when their profile states one, else their current job.                           |
| `location`                                                                                                | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `profileUrl`                                                                                              | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `imageUrl`                                                                                                | *string*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `companyOnProfile`                                                                                        | [operations.CompanyOnProfile](../../models/operations/company-on-profile.md)                              | :heavy_check_mark:                                                                                        | Whether their own profile names the company now, before, or not yet: a profile can lag the news by weeks. |
| `contactId`                                                                                               | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |
| `avatarUrl`                                                                                               | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |