# InboxMessagesSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { InboxMessagesSpent } from "bereach/models/operations";

let value: InboxMessagesSpent = {
  amount: 1369.17,
  currency: "USD",
  text: "<value>",
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `amount`                                                                               | *number*                                                                               | :heavy_check_mark:                                                                     | The money spent.                                                                       |
| `currency`                                                                             | [operations.InboxMessagesCurrency](../../models/operations/inbox-messages-currency.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `text`                                                                                 | *string*                                                                               | :heavy_check_mark:                                                                     | The amount as a person reads it, with its currency.                                    |