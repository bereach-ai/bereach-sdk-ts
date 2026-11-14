# ContactsCheckFitResponse

How many people were scored

## Example Usage

```typescript
import { ContactsCheckFitResponse } from "bereach/models/operations";

let value: ContactsCheckFitResponse = {
  success: true,
  checked: 596914,
  scored: 202392,
  failedBatches: 35256,
  skipped: 461222,
  setup: {
    icp: "<value>",
    personas: [],
  },
  creditsUsed: 6758.56,
  spent: {
    amount: 6436.28,
    currency: "USD",
    text: "<value>",
  },
  cost: {
    amount: 7286.41,
    currency: "EUR",
    text: "<value>",
  },
};
```

## Fields

| Field                                                                                                                         | Type                                                                                                                          | Required                                                                                                                      | Description                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                     | *true*                                                                                                                        | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `checked`                                                                                                                     | *number*                                                                                                                      | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `scored`                                                                                                                      | *number*                                                                                                                      | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `failedBatches`                                                                                                               | *number*                                                                                                                      | :heavy_check_mark:                                                                                                            | N/A                                                                                                                           |
| `skipped`                                                                                                                     | *number*                                                                                                                      | :heavy_check_mark:                                                                                                            | People past the most one check reads.                                                                                         |
| `setup`                                                                                                                       | [operations.Setup](../../models/operations/setup.md)                                                                          | :heavy_check_mark:                                                                                                            | What the people were checked against.                                                                                         |
| `started`                                                                                                                     | *boolean*                                                                                                                     | :heavy_minus_sign:                                                                                                            | N/A                                                                                                                           |
| `running`                                                                                                                     | *boolean*                                                                                                                     | :heavy_minus_sign:                                                                                                            | N/A                                                                                                                           |
| `run`                                                                                                                         | [operations.ContactsCheckFitRun](../../models/operations/contacts-check-fit-run.md)                                           | :heavy_minus_sign:                                                                                                            | N/A                                                                                                                           |
| `quote`                                                                                                                       | [operations.ContactsCheckFitQuote](../../models/operations/contacts-check-fit-quote.md)                                       | :heavy_minus_sign:                                                                                                            | N/A                                                                                                                           |
| `creditsUsed`                                                                                                                 | *number*                                                                                                                      | :heavy_check_mark:                                                                                                            | Credits the check in progress has spent so far, for code: tell the user spent, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                       | [operations.ContactsCheckFitSpent](../../models/operations/contacts-check-fit-spent.md)                                       | :heavy_check_mark:                                                                                                            | What the check in progress has spent so far, in money: the figure to tell the user.                                           |
| `cost`                                                                                                                        | [operations.ContactsCheckFitCost](../../models/operations/contacts-check-fit-cost.md)                                         | :heavy_check_mark:                                                                                                            | The most a check costs, in money: say this amount.                                                                            |
| `refused`                                                                                                                     | [operations.ContactsCheckFitRefused](../../models/operations/contacts-check-fit-refused.md)                                   | :heavy_minus_sign:                                                                                                            | N/A                                                                                                                           |
| `stopping`                                                                                                                    | *boolean*                                                                                                                     | :heavy_minus_sign:                                                                                                            | N/A                                                                                                                           |
| `listUrl`                                                                                                                     | *string*                                                                                                                      | :heavy_minus_sign:                                                                                                            | The list in the app, to give the user.                                                                                        |