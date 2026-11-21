# PublicFindSignalsItemResponse

## Example Usage

```typescript
import { PublicFindSignalsItemResponse } from "bereach/models/operations";

let value: PublicFindSignalsItemResponse = {
  event: null,
  company: "Hermann - Crist",
  companyPage: "<value>",
  people: [],
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `event`                                                                                               | [operations.ItemEvent](../../models/operations/item-event.md)                                         | :heavy_check_mark:                                                                                    | The event this company was read in, as it was returned. Null when no known event id was given.        |
| `company`                                                                                             | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `companyPage`                                                                                         | *string*                                                                                              | :heavy_check_mark:                                                                                    | The company's LinkedIn page. Null when none was found, and then nobody is returned for this company.  |
| `people`                                                                                              | [operations.PublicFindSignalsPerson](../../models/operations/public-find-signals-person.md)[]         | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `note`                                                                                                | *string*                                                                                              | :heavy_minus_sign:                                                                                    | Why nobody came back for this company, or what the people shown are when that needs saying. Relay it. |