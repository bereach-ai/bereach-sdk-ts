# ScheduledMessageListSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { ScheduledMessageListSpent } from "bereach/models/operations";

let value: ScheduledMessageListSpent = {
  amount: 1181.76,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `amount`                                                                                              | *number*                                                                                              | :heavy_check_mark:                                                                                    | The money spent.                                                                                      |
| `currency`                                                                                            | [operations.ScheduledMessageListCurrency](../../models/operations/scheduled-message-list-currency.md) | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `text`                                                                                                | *string*                                                                                              | :heavy_check_mark:                                                                                    | The amount as a person reads it, with its currency.                                                   |