# ContactsAddSignalsQuote

## Example Usage

```typescript
import { ContactsAddSignalsQuote } from "bereach/models/operations";

let value: ContactsAddSignalsQuote = {
  kind: "email",
  people: 908178,
  alreadyDone: 602784,
  credits: 8165.65,
  confirm: false,
  affordable: true,
  affordablePeople: 306251,
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `kind`                                                                                                    | [operations.ContactsAddSignalsQuoteKind](../../models/operations/contacts-add-signals-quote-kind.md)      | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `people`                                                                                                  | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `alreadyDone`                                                                                             | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `credits`                                                                                                 | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `creditsLeft`                                                                                             | *number*                                                                                                  | :heavy_minus_sign:                                                                                        | What is left in the pool, on the app's own panel only: an API key or the connector never reads a balance. |
| `confirm`                                                                                                 | *boolean*                                                                                                 | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `affordable`                                                                                              | *boolean*                                                                                                 | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `affordablePeople`                                                                                        | *number*                                                                                                  | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `extra`                                                                                                   | Record<string, *number*>                                                                                  | :heavy_minus_sign:                                                                                        | N/A                                                                                                       |