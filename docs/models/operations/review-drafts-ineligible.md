# ReviewDraftsIneligible

Ids that were not in draft, with the status they were in.

## Example Usage

```typescript
import { ReviewDraftsIneligible } from "bereach/models/operations";

let value: ReviewDraftsIneligible = {
  approved: [],
  rejected: [
    {
      id: "<id>",
      currentStatus: null,
    },
  ],
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `approved`                                                   | [operations.Approved](../../models/operations/approved.md)[] | :heavy_check_mark:                                           | N/A                                                          |
| `rejected`                                                   | [operations.Rejected](../../models/operations/rejected.md)[] | :heavy_check_mark:                                           | N/A                                                          |