# ContactPosition

## Example Usage

```typescript
import { ContactPosition } from "bereach/models/operations";

let value: ContactPosition = {
  companyName: "Lebsack, Skiles and Connelly",
  title: null,
  companyUrl: "https://ajar-curl.net",
  startDate: {
    year: 3032.77,
  },
  endDate: {
    year: 6625.91,
  },
  isCurrent: false,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `companyName`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `title`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `companyUrl`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `startDate`                                                                                   | [operations.ContactPositionStartDate](../../models/operations/contact-position-start-date.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `endDate`                                                                                     | [operations.ContactPositionEndDate](../../models/operations/contact-position-end-date.md)     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `isCurrent`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |