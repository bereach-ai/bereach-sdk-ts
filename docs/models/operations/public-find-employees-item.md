# PublicFindEmployeesItem

## Example Usage

```typescript
import { PublicFindEmployeesItem } from "bereach/models/operations";

let value: PublicFindEmployeesItem = {
  name: "<value>",
  headline: "<value>",
  currentTitle: "<value>",
  location: "<value>",
  profileUrl: "https://junior-minority.info",
  imageUrl: "https://leading-convection.com/",
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `name`                                                                                              | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `headline`                                                                                          | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `currentTitle`                                                                                      | *string*                                                                                            | :heavy_check_mark:                                                                                  | Their job at this company, when they state one.                                                     |
| `location`                                                                                          | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `profileUrl`                                                                                        | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `imageUrl`                                                                                          | *string*                                                                                            | :heavy_check_mark:                                                                                  | N/A                                                                                                 |
| `employer`                                                                                          | [operations.PublicFindEmployeesEmployer](../../models/operations/public-find-employees-employer.md) | :heavy_minus_sign:                                                                                  | The person's current employer, from that company's own record, when one was read for them.          |
| `completeness`                                                                                      | [operations.Completeness](../../models/operations/completeness.md)                                  | :heavy_minus_sign:                                                                                  | Present when this person was already in your contacts: returned again at no cost.                   |
| `contactId`                                                                                         | *string*                                                                                            | :heavy_minus_sign:                                                                                  | The saved contact's id: the id the email and phone lookups take.                                    |
| `avatarUrl`                                                                                         | *string*                                                                                            | :heavy_minus_sign:                                                                                  | The saved contact's photo, when there is one.                                                       |