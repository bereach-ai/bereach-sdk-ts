# VisitProfilePosition

## Example Usage

```typescript
import { VisitProfilePosition } from "bereach/models/operations";

let value: VisitProfilePosition = {
  companyName: "Upton Group",
  title: "<value>",
  companyUrl: "https://indelible-summer.info",
  companyLogo: "<value>",
  startDate: {
    month: 435097,
    year: 83382,
  },
  endDate: {
    month: 842462,
    year: 44039,
  },
  isCurrent: true,
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `companyName`                                                                                            | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `title`                                                                                                  | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `description`                                                                                            | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | Position description / responsibilities text. Null when there is none or the read did not answer.        |
| `companyUrl`                                                                                             | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `companyLogo`                                                                                            | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `companyDescription`                                                                                     | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | Short description of the company. May be null.                                                           |
| `startDate`                                                                                              | [operations.VisitProfilePositionStartDate](../../models/operations/visit-profile-position-start-date.md) | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `endDate`                                                                                                | [operations.VisitProfilePositionEndDate](../../models/operations/visit-profile-position-end-date.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `isCurrent`                                                                                              | *boolean*                                                                                                | :heavy_check_mark:                                                                                       | N/A                                                                                                      |