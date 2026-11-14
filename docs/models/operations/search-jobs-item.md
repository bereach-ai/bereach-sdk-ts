# SearchJobsItem

## Example Usage

```typescript
import { SearchJobsItem } from "bereach/models/operations";

let value: SearchJobsItem = {
  type: "JOB",
  title: "<value>",
  company: "Heaney - Lynch",
  companyUrl: "https://content-reasoning.name/",
  companyLogo: "<value>",
  location: null,
  workplaceType: "<value>",
  postedAt: null,
  jobUrl: "https://busy-draw.org/",
  listingId: "<id>",
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `type`                                                                   | [operations.SearchJobsType](../../models/operations/search-jobs-type.md) | :heavy_check_mark:                                                       | N/A                                                                      |
| `title`                                                                  | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `company`                                                                | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `companyUrl`                                                             | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `companyLogo`                                                            | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `location`                                                               | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `workplaceType`                                                          | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `postedAt`                                                               | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `jobUrl`                                                                 | *string*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `listingId`                                                              | *string*                                                                 | :heavy_check_mark:                                                       | LinkedIn job listing id.                                                 |