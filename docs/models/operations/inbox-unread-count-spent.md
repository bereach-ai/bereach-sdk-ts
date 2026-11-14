# InboxUnreadCountSpent

What this call spent, in money: the figure to tell the user, written as text says it.

## Example Usage

```typescript
import { InboxUnreadCountSpent } from "bereach/models/operations";

let value: InboxUnreadCountSpent = {
  amount: 9596.79,
  currency: "EUR",
  text: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `amount`                                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | The money spent.                                                                              |
| `currency`                                                                                    | [operations.InboxUnreadCountCurrency](../../models/operations/inbox-unread-count-currency.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `text`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | The amount as a person reads it, with its currency.                                           |