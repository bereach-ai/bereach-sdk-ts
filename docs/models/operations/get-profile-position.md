# GetProfilePosition

## Example Usage

```typescript
import { GetProfilePosition } from "bereach/models/operations";

let value: GetProfilePosition = {
  companyName: "Homenick, Heaney and Abernathy",
  title: "<value>",
  companyUrl: "https://steel-vein.org/",
  companyLogo: "<value>",
  startDate: {
    month: 960904,
    year: 39923,
  },
  endDate: {
    month: 724500,
    year: 533733,
  },
  isCurrent: false,
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `companyName`                                                                                        | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `title`                                                                                              | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `description`                                                                                        | *string*                                                                                             | :heavy_minus_sign:                                                                                   | Position description / responsibilities text. Null when there is none or the read did not answer.    |
| `companyUrl`                                                                                         | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `companyLogo`                                                                                        | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `companyDescription`                                                                                 | *string*                                                                                             | :heavy_minus_sign:                                                                                   | Short description of the company. May be null.                                                       |
| `startDate`                                                                                          | [operations.GetProfilePositionStartDate](../../models/operations/get-profile-position-start-date.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `endDate`                                                                                            | [operations.GetProfilePositionEndDate](../../models/operations/get-profile-position-end-date.md)     | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `isCurrent`                                                                                          | *boolean*                                                                                            | :heavy_check_mark:                                                                                   | N/A                                                                                                  |