# ScheduledMessageUpdateSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ScheduledMessageUpdateSpent } from "bereach/models/operations";

let value: ScheduledMessageUpdateSpent = {
  amount: 2612.87,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                  | *number*                                                                                                  | :heavy_check_mark:                                                                                        | The money spent.                                                                                          |
| `currency`                                                                                                | [operations.ScheduledMessageUpdateCurrency](../../models/operations/scheduled-message-update-currency.md) | :heavy_check_mark:                                                                                        | N/A                                                                                                       |
| `text`                                                                                                    | *string*                                                                                                  | :heavy_check_mark:                                                                                        | The amount as a person reads it, with its currency.                                                       |