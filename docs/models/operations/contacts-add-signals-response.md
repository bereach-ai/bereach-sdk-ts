# ContactsAddSignalsResponse

Whether a run started, the last run, and the quote

## Example Usage

```typescript
import { ContactsAddSignalsResponse } from "bereach/models/operations";

let value: ContactsAddSignalsResponse = {
  started: false,
  running: false,
  progress: null,
  people: 697187,
  companies: 315619,
  credits: 1347.21,
  cost: {
    amount: 9853.73,
    currency: "USD",
    text: "<value>",
  },
  creditsUsed: 6279.44,
  spent: {
    amount: 5960.12,
    currency: "EUR",
    text: "<value>",
  },
  run: {
    id: "<id>",
    kind: "reasons",
    state: "failed",
    total: 729810,
    done: 88478,
    found: 668990,
    none: 801439,
    failed: 60320,
    skipped: 240917,
    credits: 6476.47,
    creditsMax: 2880.71,
    startedAt: "<value>",
  },
  quote: {
    kind: "reasons",
    people: 84257,
    alreadyDone: 427603,
    credits: 6569.94,
    confirm: false,
    affordable: false,
    affordablePeople: 757651,
  },
};
```

## Fields

| Field                                                                                                                       | Type                                                                                                                        | Required                                                                                                                    | Description                                                                                                                 |
| --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| `started`                                                                                                                   | *boolean*                                                                                                                   | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `running`                                                                                                                   | *boolean*                                                                                                                   | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `progress`                                                                                                                  | [operations.Progress](../../models/operations/progress.md)                                                                  | :heavy_check_mark:                                                                                                          | The run this call started, else the last run, or null when the list never had one.                                          |
| `people`                                                                                                                    | *number*                                                                                                                    | :heavy_check_mark:                                                                                                          | People a run reads.                                                                                                         |
| `companies`                                                                                                                 | *number*                                                                                                                    | :heavy_check_mark:                                                                                                          | Their distinct companies, one news search each.                                                                             |
| `credits`                                                                                                                   | *number*                                                                                                                    | :heavy_check_mark:                                                                                                          | The most a run costs, in credits, for code: tell the user cost, never this number.                                          |
| `cost`                                                                                                                      | [operations.ContactsAddSignalsCost](../../models/operations/contacts-add-signals-cost.md)                                   | :heavy_check_mark:                                                                                                          | The most a run costs, in money: say this amount.                                                                            |
| `creditsUsed`                                                                                                               | *number*                                                                                                                    | :heavy_check_mark:                                                                                                          | Credits the run in progress has spent so far, for code: tell the user spent, never this number. 0 when nothing was charged. |
| `spent`                                                                                                                     | [operations.ContactsAddSignalsSpent](../../models/operations/contacts-add-signals-spent.md)                                 | :heavy_check_mark:                                                                                                          | What the run in progress has spent so far, in money: the figure to tell the user.                                           |
| `run`                                                                                                                       | [operations.ContactsAddSignalsRun](../../models/operations/contacts-add-signals-run.md)                                     | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `quote`                                                                                                                     | [operations.ContactsAddSignalsQuote](../../models/operations/contacts-add-signals-quote.md)                                 | :heavy_check_mark:                                                                                                          | N/A                                                                                                                         |
| `refused`                                                                                                                   | [operations.ContactsAddSignalsRefused](../../models/operations/contacts-add-signals-refused.md)                             | :heavy_minus_sign:                                                                                                          | N/A                                                                                                                         |
| `stopping`                                                                                                                  | *boolean*                                                                                                                   | :heavy_minus_sign:                                                                                                          | N/A                                                                                                                         |
| `listUrl`                                                                                                                   | *string*                                                                                                                    | :heavy_minus_sign:                                                                                                          | The list in the app, to give the user.                                                                                      |